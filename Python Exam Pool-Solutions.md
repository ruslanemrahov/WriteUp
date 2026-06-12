Göndərdiyiniz siyahıda təkrar olunan sualları (funksiyaları) qruplaşdırıb, hər birinin altına müvafiq Python kodunu əlavə etdim.

---

### `list_sum(lst)`

* S1: list_sum(lst) - siyahidaki adedlerin cemini qaytarsin
* S9: list_sum(lst) funksiyasini yazin
* S17: list_sum(lst) - siyahidaki butun adedleri toplayin
* S22: list_sum(lst) funksiyasini yazin
* S30: list_sum(lst) - siyahidaki adedlerin cemini tapin
* S39: list_sum(lst) funksiyasini yazin
* S48: list_sum(lst) - siyahidaki adedlerin cemini qaytarsin
* S56: list_sum(lst) funksiyasini yazin

```python
def list_sum(lst):
    return sum(lst)

```

---

### `flatten(lst)`

* S2: flatten(lst) - bir seviyyeli ic-ice siyahini duz siyahiya cevirsin
* S14: flatten(lst) funksiyasini yazin
* S23: flatten(lst) - bir seviyyeli ic-ice siyahini duz siyahiya cevirin
* S35: flatten(lst) - bir seviyyeli ic-ice siyahini duz siyahiya cevirin
* S49: flatten(lst) - bir seviyyeli ic-ice siyahini duz siyahiya cevirin
* S57: flatten(lst) - bir seviyyeli ic-ice siyahini duz siyahiya cevirin
* S60: bir seviyyeli ic-ice siyahini duz siyahiya cevirin (tekrar)

```python
def flatten(lst):
    result = []
    for item in lst:
        if isinstance(item, list):
            result.extend(item)
        else:
            result.append(item)
    return result

```

---

### `count_vowels(s)`

* S3: count_vowels(s) - setirdeki saitlerin sayini qaytarsin
* S13: count_vowels(s) funksiyasini yazin
* S18: count_vowels(s) - saitlerin sayini tapin
* S26: count_vowels(s) funksiyasini yazin
* S34: count_vowels(s) funksiyasini yazin
* S44: count_vowels(s) funksiyasini yazin
* S52: count_vowels(s) funksiyasini yazin

```python
def count_vowels(s):
    vowels = "aeiouAEIOU"
    return sum(1 for c in s if c in vowels)

```

---

### `find_max(lst)`

* S5: find_max(lst) - siyahidaki en boyuk adedi qaytarsin
* S10: find_max(lst) - siyahidaki en boyuk adedi tapin
* S19: find_max(lst) - siyahidaki en boyuk adedi qaytarin
* S31: find_max(lst) - siyahidaki en boyuk adedi qaytarin

```python
def find_max(lst):
    max_val = lst[0]
    for n in lst:
        if n > max_val:
            max_val = n
    return max_val

```

---

### `split_parity(lst)`

* S6: split_parity(lst) - siyahidaki adedleri tek ve cut olaraq ayirsin
* S20: split_parity(lst) - siyahidaki adedleri tek ve cut olaraq ayirin
* S32: split_parity(lst) - siyahidaki adedleri tek ve cut olaraq ayirin
* S46: split_parity(lst) - siyahidaki adedleri tek ve cut olaraq ayirin
* S58: split_parity(lst) - siyahidaki adedleri tek ve cut olaraq ayirin

```python
def split_parity(lst):
    odd = [n for n in lst if n % 2 != 0]
    even = [n for n in lst if n % 2 == 0]
    return (odd, even)

```

---

### `common_words(sent1, sent2)`

* S7: common_words(sent1, sent2) - iki cumlede ortaq sozleri tapin
* S24: common_words(sent1, sent2) - iki cumlede ortaq sozleri tapin
* S36: common_words(sent1, sent2) - iki cumlede ortaq sozleri tapin
* S38: iki cumlede ortaq sozleri tapin (tekrar)

```python
def common_words(sent1, sent2):
    set1 = set(sent1.split())
    set2 = set(sent2.split())
    return set1 & set2

```

---

### `unique_words_by_length(words)` / `unique_words(lst)`

* S11: unique_words(lst) - 10 sozden unikal sozleri tapin ve uzunluga gore sirala
* S28: unique_words_by_length(words) - unikal sozleri tapin ve uzunluga gore sirala
* S40: unique_words_by_length(words) - unikal sozleri tapin ve uzunluga gore sirala
* S50: unique_words_by_length(words) - unikal sozleri tapin ve uzunluga gore sirala

```python
def unique_words_by_length(words):
    unique = list(set(words))
    unique.sort(key=len)
    return unique

```

---

### `rock_paper_scissors(player1, player2)`

* S12: rock_paper_scissors(player1, player2) - qalibi mueyyen edin
* S29: rock_paper_scissors(player1, player2) - qalibi mueyyen edin
* S42: rock_paper_scissors(player1, player2) - qalibi mueyyen edin
* S43: rock_paper_scissors(player1, player2) (tekrar)
* S51: rock_paper_scissors(player1, player2) - qalibi mueyyen edin

```python
def rock_paper_scissors(player1, player2):
    if player1 == player2:
        return "Draw"
    beats = {"rock": "scissors", "scissors": "paper", "paper": "rock"}
    if beats[player1] == player2:
        return "Player1 wins"
    else:
        return "Player2 wins"

```

---

### `set_difference(s1, s2)`

* S15: set_difference(s1,s2) - yalniz birinci setde olan elementleri qaytarin
* S27: set_difference(s1,s2) - yalniz birinci setde olan elementleri qaytarin
* S45: set_difference(s1,s2) - yalniz birinci setde olan elementleri qaytarin
* S53: set_difference(s1,s2) - yalniz birinci setde olan elementleri qaytarin

```python
def set_difference(s1, s2):
    return s1 - s2

```

---

### `collatz_sequence(n)`

* S16: collatz_sequence(n) - N alin, cutdirse N/2, tekdirse 3N+1, N=1 olana qeder davam edin
* S25: collatz_sequence(n) - N alin, tekdirse 3N+1, cutdurse N/2, N=1 olana qeder davam edin
* S37: collatz_sequence(n) - N daxil edin, cutdurse N/2, tekdirse 3N+1, N=1 olana qeder davam edin
* S55: collatz_sequence(n) - N daxil edin, cutdurse N/2, tekdirse 3N+1, N=1 olana qeder davam edin

```python
def collatz_sequence(n):
    steps = [n]
    while n != 1:
        if n % 2 == 0:
            n = n // 2
        else:
            n = 3 * n + 1
        steps.append(n)
    for s in steps:
        print(s)
    return steps

```

---

### `fibonacci_sum_even(n)`

* S21: fibonacci_sum_even(n) - ilk N Fibonacci adedini yaradin ve cut elementlerin cemini qaytarin
* S47: fibonacci_sum_even(n) - ilk N Fibonacci adedini yaradin ve cut elementlerin cemini qaytarin
* S59: fibonacci_sum_even(n) - ilk N Fibonacci adedini yaradin ve cut elementlerin cemini qaytarin

```python
def fibonacci_sum_even(n):
    fib = [0, 1]
    for i in range(2, n):
        fib.append(fib[-1] + fib[-2])
    fib = fib[:n]
    return sum(x for x in fib if x % 2 == 0)

```

---

### `find_common_letters(str1, str2)`

* S41: find_common_letters(str1, str2) - iki stringde ortaq herfleri tapin
* S54: find_common_letters(str1,str2) - iki stringde ortaq herfleri tapin

```python
def find_common_letters(str1, str2):
    return set(str1) & set(str2)

```
