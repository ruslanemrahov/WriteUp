# Süni İntellekt (İPFS-B10) — Final İmtahan Sualları və Ətraflı Cavablar

---

## MÖVZu 1: Süni İntellektə Giriş

---

### Sual 1 (Praktiki)

**Sual:** Ardıcıl olaraq aşağıdakı kodlar icra olunur:
```python
x = 7
hesab = x ** 2
müqayisə = hesab < 50
print(müqayisə)
```
Ekrana hansı dəyər çıxacaq və müqayisənin doğruluğunu izah edin.

**Cavab:**

Kodun icra ardıcıllığını addım-addım izləyək:

1. `x = 7` — İlk olaraq `x` dəyişəninə `7` tam ədədi mənimsədilir. Yaddaşda `x` adlı bir qutu açılır və ora 7 rəqəmi yerləşdirilir.

2. `hesab = x ** 2` — `**` operatoru Python-da **qüvvətə yüksəltmə** (eksponent) operatorudur. Yəni `x ** 2` ifadəsi `x`-in kvadratını hesablayır: `7 ** 2 = 7 × 7 = 49`. Nəticə olaraq `hesab` dəyişəninə `49` dəyəri mənimsədilir.

3. `müqayisə = hesab < 50` — Bu sətirdə `<` (kiçikdir) müqayisə operatoru istifadə olunur. `hesab`-ın dəyəri `49`-dur. Sual belədir: `49 < 50` doğrudurmu? Bəli, 49 həqiqətən 50-dən kiçikdir. Buna görə də bu müqayisənin nəticəsi **`True`** (Boolean — məntiqi doğru) olacaq. `müqayisə` dəyişəninə `True` dəyəri mənimsədilir.

4. `print(müqayisə)` — Ekrana `müqayisə` dəyişəninin dəyəri, yəni **`True`** çap olunur.

**Nəticə:** Ekrana `True` çıxacaq. Əgər `x = 8` olsaydı, `8 ** 2 = 64` olardı və `64 < 50` yanlış olduğundan `False` çıxardı.

---

### Sual 2 (Praktiki)

**Sual:** `x = 14` üçün aşağıdakı kod:
```python
x = 14
netice = (x % 2 == 0) & (x > 10) & (x < 20)
print(netice)
```
Hər şərti mərhələli icra edin. Əgər `x = 21` olsaydı fərq nə olardı?

**Cavab:**

**`x = 14` üçün icra:**

- **Şərt 1:** `x % 2 == 0` → `14 % 2 = 0` (14 cütdür, qalıq yoxdur) → `0 == 0` → **True**
- **Şərt 2:** `x > 10` → `14 > 10` → **True**
- **Şərt 3:** `x < 20` → `14 < 20` → **True**

`&` operatoru bitwise AND (AND məntiqi) əməliyyatı aparır. Boolean dəyərlər üzərindəki qaydası belədir: `True & True & True = True`.

Nəticə: `netice = True` → ekrana `True` çap olunur.

**`x = 21` olsaydı:**

- **Şərt 1:** `21 % 2 == 0` → `21 % 2 = 1` → `1 == 0` → **False**
- **Şərt 2:** `21 > 10` → **True**
- **Şərt 3:** `21 < 20` → **False**

`False & True & False = False`

Fərqlilik **birinci addımdan** başlayır: 21 cüt ədəd deyil, buna görə ilk şərt `False` qaytarır. `&` operatorunun məntiq qapısı (AND gate) xüsusiyyəti belədir: bütün operandlar `True` olmadığı halda nəticə mütləq `False` olur. Hər üç şərtin hamısının eyni anda doğru olması tələb olunduğundan, birinin belə `False` olması bütün ifadəni `False` edir.

---

### Sual 3 (Praktiki)

**Sual:** `metn = 'python proqramlasdirma-dili'` sətrinə 3 metod tətbiq etsək nə olar?
```python
metn = metn.replace('-', ' ')
metn = metn.upper()
nəticə = metn.split()
```

**Cavab:**

**Addım 1 — `.replace('-', ' ')`:**
`.replace(köhnə, yeni)` metodu sətirdəki bütün köhnə simvolları yeni simvolla əvəzləyir. Burada tire (`-`) simvolu boşluq (` `) ilə əvəzlənir:
- Əvvəl: `'python proqramlasdirma-dili'`
- Sonra: `'python proqramlasdirma dili'`

Tire aradan çıxır, onun yerini boşluq alır.

**Addım 2 — `.upper()`:**
`.upper()` metodu sətirdəki bütün kiçik hərfləri böyük hərflərə çevirir:
- Əvvəl: `'python proqramlasdirma dili'`
- Sonra: `'PYTHON PROQRAMLASDIRMA DILI'`

**Addım 3 — `.split()`:**
`.split()` metodu sətiri boşluqlara görə parçalayır və bir **siyahı (list)** qaytarır:
- `'PYTHON PROQRAMLASDIRMA DILI'` → `['PYTHON', 'PROQRAMLASDIRMA', 'DILI']`

**Məlumat növünün dəyişməsi:** İlk iki əməliyyatdan sonra `metn` yenə `str` (sətir) tipindədir. Lakin `.split()` tətbiq edildiyi andan `nəticə` dəyişəninin tipi `list` (siyahı) olur. Yəni sətir parçalanır və hər söz ayrı bir element kimi siyahıya düşür.

---

### Sual 4 (Praktiki)

**Sual:** `kod_setri = 'A-1-B-2-C-3-D'` sətrinə ardıcıl 3 əməliyyat: tərsinə çevirm, tire silmə, kiçik hərflərə çevirməni bir sətirdə yazın və `[::-1]` prosesini izah edin.

**Cavab:**

**Bir sətirdə həll:**
```python
nəticə = kod_setri[::-1].replace('-', ' ').lower()
```

**`[::-1]` prosesinin işləmə mexanizmi:**

Python-da dilimləmə (slicing) sintaksisi `[başlanğıc:son:addım]` şəklindədir. `[::-1]` ifadəsindəki mənfi addım (`-1`) prosessora deyir ki: "sətrin **sonuncu indeksindən başla** və hər dəfə bir addım **geriyə** get".

Orijinal sətir: `A - 1 - B - 2 - C - 3 - D` (indekslər 0-dan 12-yə qədər)

- Mənfi addım parametri sətirin sonuncu elementindən (indeks 12, `D`) başlayır
- Hər addımda bir element sola (geriyə) hərəkət edir
- `D` → `3` → `-` → `C` → `2` → `-` → `B` → `1` → `-` → `A` ardıcıllığı ilə oxuyur

Nəticə: `'D-3-C-2-B-1-A'`

**3 addım ardıcıl:**
1. `kod_setri[::-1]` → `'D-3-C-2-B-1-A'`
2. `.replace('-', ' ')` → `'D 3 C 2 B 1 A'`
3. `.lower()` → `'d 3 c 2 b 1 a'`

**Yaddaşa təsiri:** Hər metod çağrısı yeni bir sətir obyekti yaradır (çünki Python-da sətrlər dəyişməzdir — immutable). Orijinal `kod_setri` dəyişdirilmir, yeni `nəticə` dəyişəninə son hal mənimsədilir. Zəncirvari yazımda hər ara nəticə müvəqqəti yaddaşda saxlanılır, növbəti metod ona tətbiq edilir.

---

### Sual 5 (Praktiki)

**Sual:** `list_1 = [1, 2, 3]` və `tuple_1 = (1, 2, 3)` — hər ikisinin 0-cı indeksini 10 ilə əvəzləməyə çalışdıqda nə olur? Tuple-List fərqini izah edin.

**Cavab:**

**List üçün:**
```python
list_1[0] = 10  # Bu işləyir!
# list_1 = [10, 2, 3]
```
Siyahılar **mutable** (dəyişdirilə bilən) strukturlardır. İndeks vasitəsilə istənilən element yenilənə bilər. Yaddaşda `list_1[0]`-ın göstərdiyi yer 1-dən 10-a yenilənir.

**Tuple üçün:**
```python
tuple_1[0] = 10  # Bu XƏTA verir!
# TypeError: 'tuple' object does not support item assignment
```
Kortejlər **immutable** (dəyişdirilə bilməyən) strukturlardır. Bir dəfə yaradıldıqdan sonra onların heç bir elementi dəyişdirilə, silinə və ya əlavə edilə bilməz. Python interpretatoru bu cəhdi aşkar etdikdə dərhal `TypeError` xətası qaldırır.

**Tuple vs List — əsas fərqlər:**

| Xüsusiyyət | List `[]` | Tuple `()` |
|---|---|---|
| Dəyişdirilə bilmə | Bəli (Mutable) | Xeyr (Immutable) |
| Yaddaş sərfiyyatı | Daha çox | Daha az |
| Sürət | Biraz yavaş | Daha sürətli |
| Sintaksis | `[1, 2, 3]` | `(1, 2, 3)` |

**Tuple-ların proqramlaşdırmada istifadə məqsədləri:**
- Dəyişdirilməməsi lazım olan sabit konfiqurasiya məlumatlarını saxlamaq üçün (məsələn, koordinatlar, RGB rənk dəyərləri)
- Dictionary açarı kimi istifadə etmək üçün (list açar ola bilməz, tuple isə hashable-dır)
- Funksiyadan birdən çox dəyər qaytarmaq üçün (`return x, y` əslində tuple qaytarır)
- Məlumatın təsadüfən dəyişdirilməsinin qarşısını almaq üçün

---

## MÖVZu 2: Süni İntellekt Tətbiqi

---

### Sual 6 (Praktiki)

**Sual:** Aşağıdakı kod:
```python
x = 7
if x >= 9:
    print('A xal')
elif x > 5:
    print('B xal')
else:
    print('C xal')
```
Nə çap olunur? `elif` strukturu ilə iki ayrı `if` strukturunun fərqini izah edin.

**Cavab:**

**Kod icrasının analizi (`x = 7`):**

- `if x >= 9:` → `7 >= 9` → **False** → bu blok keçilir
- `elif x > 5:` → `7 > 5` → **True** → bu blok icra olunur
- Ekrana **`B xal`** çap olunur
- `else` bloku artıq yoxlanılmır

**`if-elif-else` vs. ardıcıl `if-if` strukturunun mexaniki fərqi:**

`if-elif-else` (şaxəli struktur) — **bir blok icra edildikdən sonra digərləri BÜTÜNLÜKLƏ atlanır**. Bu, bir qapı mexanizmi kimidir: birinci açıq qapıdan girildikdən sonra qalan qapılar bağlanır.

```python
# if-elif: x = 10 olduqda
if x >= 9:
    print('A xal')  # Bu icra olunur, sonrası atlanır
elif x > 5:
    print('B xal')  # Bu BAXILMAZ
```

Ardıcıl `if-if` (müstəqil strukturlar) — **hər `if` müstəqil olaraq yoxlanılır**. Birinin doğru olması digərinin yoxlanılmasını dayandırmır.

```python
# iki ayrı if: x = 10 olduqda
if x >= 9:
    print('A xal')  # Bu icra olunur
if x > 5:
    print('B xal')  # Bu DA icra olunur!
```

Nəticə: `x = 10` olduqda `if-elif` yalnız `A xal` çap edir, iki ayrı `if` isə həm `A xal`, həm də `B xal` çap edir. Bu mühüm fərq xüsusilə bir dəfəlik seçim tələb edən hallarda kritikdir.

---

### Sual 7 (Praktiki)

**Sual:** `z = 1` ilə başlayan bu sikl:
```python
while z < 3:
    print(z)
    z += 1
```
Neçə dəfə çap olunur? `z`-nin son dəyəri nə olur? `z += 1` olmasaydı nə baş verərdi?

**Cavab:**

**Siklın addım-addım icrası:**

- **1-ci iterasiya:** `z = 1` → `1 < 3` → True → `print(1)` → `z += 1` → `z = 2`
- **2-ci iterasiya:** `z = 2` → `2 < 3` → True → `print(2)` → `z += 1` → `z = 3`
- **3-cü yoxlama:** `z = 3` → `3 < 3` → False → sikl **dayanır**

**Ekrana çap olunan dəyərlər:** `1` və `2` — cəmi **2 dəfə** çap olunur.

**Siklın bitməsindən sonra `z`-nin dəyəri:** `z = 3` yaddaşda qalır. Şərt `z < 3` olduğu üçün `z = 3` olduqda `3 < 3` artıq `False` olur və sikl dayanır. Lakin `z`-nin yaddaşdaki son dəyəri **3**-dür.

**`z += 1` olmasaydı nə baş verərdi — Sonsuz Sikl (Infinite Loop):**

Əgər `z += 1` sətri olmasaydı, `z` heç vaxt dəyişməzdi. `z = 1` olaraq qalardı və `1 < 3` şərti həmişə `True` olardı. Proqram `1`-i sonsuz olaraq ekrana çap edərdi, heç vaxt dayanmazdı. Bu vəziyyətə **sonsuz sikl (infinite loop)** deyilir. Proqram yaddaşı tükənənədək və ya istifadəçi Ctrl+C ilə dayandıranadək işləməyə davam edərdi.

---

### Sual 8 (Praktiki)

**Sual:** Dörd sütunlu Pandas DataFrame `df_2` üzərindəki iç-içə dövr:
```python
for c in range(df_2.shape[1]):
    for r in range(df_2.shape[0]):
        if df_2.iloc[r, c] % 2 == 0:
            print(f"{c}.sütun və {r}.sətir: {df_2.iloc[r, c]}")
```
`shape[1]` vs `shape[0]` nədir? `c = 0`-da dövr nəyi tarayır? Sıralamanı tərsinə çevrilsəydi nə dəyişərdi?

**Cavab:**

**`shape[0]` və `shape[1]` nədir:**

Pandas DataFrame-də `.shape` xassəsi `(sətir_sayı, sütun_sayı)` formatında bir tuple qaytarır. Buna görə:
- `df_2.shape[0]` — sətirlərin sayı (row count)
- `df_2.shape[1]` — sütunların sayı (column count)

Nümunə: 10 sətir, 4 sütunlu DataFrame üçün `.shape = (10, 4)`, `shape[0] = 10`, `shape[1] = 4`.

**`c = 0` olduqda dövr hansı istiqamətdə hərəkət edir:**

Xarici dövr `c` sütunu sabit saxlayır (`c = 0`), daxili dövr isə `r`-i 0-dan `shape[0]-1`-ə qədər dəyişdirir. Yəni proqram əvvəlcə **0-cı sütunun bütün sətirlərini yuxarıdan aşağıya tarayır**. Bu, matrisin **sütun-əsaslı (column-major)** oxunuşudur. `c = 1`-ə keçmək üçün daxili dövr tam bitməlidir — yəni 0-cı sütunun bütün elementləri yoxlandıqdan sonra.

**Dövrün tam xəritəsi:**
- `c=0, r=0` → `c=0, r=1` → ... → `c=0, r=son` → **sütun dəyişir** → `c=1, r=0` → ...

**Tərsinə çevrilsəydi (`for r` xaricdə, `for c` içəridə):**

Hərəkət istiqaməti **sətir-əsaslı (row-major)** olardı:
- `r=0, c=0` → `r=0, c=1` → `r=0, c=2` → `r=0, c=3` → **sətir dəyişir** → `r=1, c=0` → ...

Hesablama nəticəsi (cüt ədədlərin çap olunması) eyni qalardı, lakin çap **ardıcıllığı** fərqli olardı: cari versiyada sütun-sütun, yeni versiyada isə sətir-sətir çap olunardı. Məsələn, eyni element `2.sütun, 3.sətir` deyil, `3.sətir, 2.sütun` olaraq oxunardı.

---

### Sual 9 (Praktiki)

**Sual:** Aşağıdakı `try-except-finally` kodu:
```python
try:
    nəticə = 10 / 0
except ZeroDivisionError:
    print('Sıfıra bölmə xətası baş verdi!')
finally:
    print('Əməliyyat dövrü tamamlandı.')
```
Ekrana ardıcıl nə çap olunur? `finally`-nin rolu nədir?

**Cavab:**

**Ekrana ardıcıl çap olunan mətnlər:**
```
Sıfıra bölmə xətası baş verdi!
Əməliyyat dövrü tamamlandı.
```

**İcra ardıcıllığı:**

1. `try` bloku icra olmağa başlayır: `10 / 0` ifadəsi hesablanır
2. Python-da hər hansı ədədi sıfıra bölmək `ZeroDivisionError` xətası yaradır
3. Xəta aşkar edildikdən sonra `try` bloku yarımçıq dayanır
4. `except ZeroDivisionError:` bloku aktiv olur və `'Sıfıra bölmə xətası baş verdi!'` çap olunur
5. `finally` bloku — xəta olsun ya olmasın — **mütləq icra olunur** və `'Əməliyyat dövrü tamamlandı.'` çap olunur

**`finally` blokunun rolu və əhəmiyyəti:**

`finally` bloku Python-da "garantiyalı icra" blokudur. Aşağıdakı hallarda belə işləyir:
- `try` blokunda xəta baş verəndə
- `except` blokunda xəta baş verəndə
- `try` blokunda `return` yazılanda belə
- Proqramın normal bitməsində

Bu blok əsasən **resurs azad etmə** (resource cleanup) üçün istifadə olunur: açıq fayl bağlanması (`file.close()`), verilənlər bazası bağlantısının qapanması (`connection.close()`), şəbəkə soketinin bağlanması. Hətta kritik xəta hallarında belə resursların düzgün azad edilməsi sistemin stabil işləməsi üçün vacibdir.

---

### Sual 10 (Praktiki)

**Sual:** Adi `for` dövrü:
```python
yeni_siyahı = []
for x in range(5):
    yeni_siyahı.append(x * 2)
```
Bunu List Comprehension ilə necə yazarsınız? Fərqi izah edin.

**Cavab:**

**List Comprehension versiyası:**
```python
yeni_siyahı = [x * 2 for x in range(5)]
```

Nəticə hər iki halda eynidir: `[0, 2, 4, 6, 8]`

**Dizayn baxımından fərq:**

Ənənəvi `for ... append()` yanaşması 3 sətir tələb edir: siyahının yaradılması, dövrün qurulması, `.append()` çağrılması. List Comprehension isə bütün bu məntiqin tək sətirdə ifadəsidir. Bu, Python-un "Pythonic" (Pythona xas) fəlsəfəsinin əyani nümunəsidir: kodun oxunaqlılığı (readability) əsas məqsəd kimi qəbul edilir.

**Kompüterin oxuma sürəti baxımından fərq:**

List Comprehension ənənəvi dövrə nisbətən bir qədər **daha sürətlidir**. Bunun səbəbi:
- `.append()` hər dövr addımında Python-da ayrıca metod çağrısı tələb edir (method call overhead)
- List Comprehension isə C dilində optimallaşdırılmış daxili mexanizmlə siyahını daha az ara əməliyyatla yaradır

Fəlsəfi baxımdan List Comprehension "nə etmək istəyirsən" sualını birbaşa cavablandırır: "0-dan 4-ə qədər hər `x` üçün `x * 2` nəticəsindən ibarət siyahı yarat." Ənənəvi versiyada isə "necə etmək lazımdır" sualının cavabı verilir: siyahı yarat, dövr qur, elementlər əlavə et. Deklarativ vs. imperativ proqramlaşdırma fərqidir.

---

## MÖVZu 3: Numpy Kitabxanası

---

### Sual 11 (Praktiki)

**Sual:** `array_5 = np.array([0, 1, 2, 3, 4, 5, 6, 7])` massivindən sonra:
```python
array_5b = array_5[4:]
array_5b[:] = 0
```
`array_5` nə olacaq? Numpy Memory View məntiqini izah edin.

**Cavab:**

**Yekun nəticə:**

```python
array_5 = [0, 1, 2, 3, 0, 0, 0, 0]
```

İlk 4 element dəyişməz qalır, sonuncu 4 element 0 olur.

**Numpy Memory View (Görünüş) Məntiqinin İzahı:**

Numpy-da dilimləmə (`array_5[4:]`) orijinal massivin **yeni bir kopyasını yaratmır**. Əvəzinə, eyni yaddaş bölgəsinə işarə edən bir **görünüş (view)** yaradır. `array_5b` müstəqil bir massiv deyil, `array_5`-in 4-cü indeksindən sonunu göstərən bir "pəncərə"dir.

Buna görə `array_5b[:] = 0` yazıldıqda:
- `array_5b`-nin işarə etdiyi yaddaq bölgəsi sıfırlanır
- Bu yaddaق bölgəsi `array_5`-in indeks 4-dən 7-yə qədər olan hissəsidir
- Nəticədə `array_5` da dəyişir

**`.copy()` istifadəsi:**

İstənməyən dəyişikliyin qarşısını almaq üçün dilimləmə zamanı `.copy()` metodu istifadə olunmalıdır:

```python
array_5b = array_5[4:].copy()  # Tam müstəqil yeni massiv yaradılır
array_5b[:] = 0                 # Bu artıq orijinalı dəyişdirmir
# array_5 = [0, 1, 2, 3, 4, 5, 6, 7]  — dəyişmir!
```

`.copy()` yaddaşda tamamilə yeni yer ayırır və dəyərləri köçürür. Artıq iki massiv arasında heç bir yaddaş bağlantısı qalmır.

---

### Sual 12 (Praktiki)

**Sual:** 6x4 ölçülü `array_8`-də `axis=0` vs `axis=1` fərqi nədir? `array_8[array_8 > 10]` nə edir — nəticə 2D olur, yoxsa 1D?

**Cavab:**

**`axis` parametrinin mənası:**

Numpy-da `axis` hesablamanın hansı istiqamətdə aparılacağını göstərir:
- `axis=0` — **sütunlar boyunca** (yuxarıdan aşağıya, sətirləri birləşdir): hər sütunun elementlərini cəmləyir → **4 ədəd dəyər** çıxır (hər sütun üçün bir cəm)
- `axis=1` — **sətirlər boyunca** (soldan sağa, sütunları birləşdir): hər sətrin elementlərini cəmləyir → **6 ədəd dəyər** çıxır (hər sətir üçün bir cəm)

Sadə xatırlama qaydası: `axis=0` "sətirləri yox edir" (sütunlar boyunca işləyir), `axis=1` "sütunları yox edir" (sətirlər boyunca işləyir).

**`array_8[array_8 > 10]` — Boolean Masking:**

Bu əmrin arxa planda işləmə mexanizmi:

1. **Maska yaradılması:** `array_8 > 10` ifadəsi orijinal massivlə eyni formada (6x4) bir Boolean massivi yaradır. 10-dan böyük hər element üçün `True`, digərlərı üçün `False` yazılır.

```
[[False, True,  True, False],
 [True,  False, True, True ],
 ...]
```

2. **Filtrləmə:** `array_8[maska]` bu Boolean maskanı indeks kimi istifadə edərək yalnız `True` olan mövqelərdəki elementləri çıxarır.

3. **Ölçü dəyişməsi:** Nəticə **həmişə 1D (bir ölçülü)** massiv olur, 2D deyil. Çünki şərtə uyğun gələn elementlərin sayı müxtəlif sütun və sətirlərdən gəlir, onları 2D formatda saxlamaq mümkün deyil (nə qədər sütun, nə qədər sətir olacağı bəlli deyil). Numpy bu elementləri düz bir sıra halında birləşdirib döndürür.

---

### Sual 13 (Praktiki)

**Sual:** `dict_avto = {'maşın': 'Kia', 'il': 2015}` lüğətinə `'rəng': 'ağ'` əlavə etmək və `'il'` silmək üçün kod yazın. Lüğətin son halı nə olacaq?

**Cavab:**

**`[]` ilə əlavə etmə:**
```python
dict_avto['rəng'] = 'ağ'
```

**`.update()` ilə əlavə etmə:**
```python
dict_avto.update({'rəng': 'ağ'})
```

Hər iki metod eyni nəticəni verir. `.update()` birdən çox açar-dəyər cütlüyünü eyni anda əlavə etmək üçün daha əlverişlidir.

**`.pop()` ilə silmə:**
```python
dict_avto.pop('il')
```

`.pop('il')` metodu `'il'` açarını və onun dəyərini (`2015`) lüğətdən silir. Əlavə olaraq, silinən dəyəri qaytarır — istəsək onu tutub saxlaya bilərik: `silinən = dict_avto.pop('il')`.

**Lüğətin son halı:**
```python
{'maşın': 'Kia', 'rəng': 'ağ'}
```

**Lüğətdə açarlarla çatmanın üstünlüyü:**

Siyahılarda elementlərə çatmaq üçün mövqe indeksi (0, 1, 2...) istifadə olunur. Bu o deməkdir ki, elementlərin ardıcıllığı dəyişərsə, indekslər də dəyişər. Lüğətlərdə isə açar dəyişməz qalır. `dict['maşın']` həmişə avtomobilin markasını qaytaracaq, lüğətin içinə nə əlavə edilsə də. Bu, kodun oxunaqlılığını artırır, xətaları azaldır və məntiqi cəhətdən daha aydın struktur yaradır.

---

### Sual 14 (Praktiki)

**Sual:** `dict_3 = {'k1': 9, 'k2': [10, 20, 30], 'k3': {'km': 125500}}`

1. `125500`-ə necə çatmaq olar?
2. `dict_3['k2']` siyahısını `3x1` Numpy 2D float massivinə çevirmək üçün kod yazın.

**Cavab:**

**Hissə 1 — `125500`-ə çatmaq:**

```python
print(dict_3['k3']['km'])
```

İzah: `dict_3['k3']` bizə `{'km': 125500}` daxili lüğətini qaytarır. Onun üzərinə dərhal `['km']` açarını tətbiq etdikdə `125500` dəyərinə çatırıq. Bu ardıcıl (zəncirvari) indeksləmə metodudur.

**Hissə 2 — Çevirmə kodu:**

```python
nəticə = np.array(dict_3['k2']).astype('float').reshape(3, 1)
```

**Hər mərhələnin izahı:**

- `dict_3['k2']` → Python siyahısı: `[10, 20, 30]`
- `np.array([10, 20, 30])` → 1D Numpy massivi: `array([10, 20, 30])`, shape: `(3,)`, tip: `int`
- `.astype('float')` → Tam ədədlər float-a çevrilir: `array([10., 20., 30.])`, tip: `float64`
- `.reshape(3, 1)` → 1D massiv 3 sətir, 1 sütunlu 2D matrisə çevrilir, shape: `(3, 1)`

**Yekun matrisin forması:**
```
[[10.]
 [20.]
 [30.]]
```
Bu, riyazi olaraq bir sütun vektoru (column vector) kimi göstərilir. Dimension: 2, Shape: (3, 1).

---

## MÖVZu 4: Pandas Kitabxanası

---

### Sual 15 (Praktiki)

**Sual:** `nums = [10, -5, 20, -3, 8]` siyahısından müsbət ədədlər:
```python
təmiz_nums = list(filter(lambda x: x > 0, nums))
```
`lambda` arxa planda necə işləyir? `təmiz_nums`-ın içi nə olacaq?

**Cavab:**

**`lambda x: x > 0` funksiyasının işləmə mexanizmi:**

`lambda` anonim (adsız) funksiyadır. `lambda x: x > 0` ifadəsi belə bir funksiya yaradır: "mənə `x` ver, mən `x > 0` şərtini yoxlayım, `True` ya da `False` qaytarım."

`filter()` funksiyası bu lambda funksiyanı `nums` siyahısındakı hər elementə ardıcıl tətbiq edir:
- `filter(lambda, 10)` → `10 > 0` → **True** → saxla
- `filter(lambda, -5)` → `-5 > 0` → **False** → at
- `filter(lambda, 20)` → `20 > 0` → **True** → saxla
- `filter(lambda, -3)` → `-3 > 0` → **False** → at
- `filter(lambda, 8)` → `8 > 0` → **True** → saxla

`filter()` obyekti lazy (tənbəl) hesablama edir — nəticəni birbaşa siyahıya çevirmir. Buna görə `list()` əlavə edilib ki, yekun nəticə siyahı formatına düşsün.

**`təmiz_nums`-ın yekun dəyəri:** `[10, 20, 8]`

---

### Sual 16 (Praktiki)

**Sual:**
```python
def f1(x): return x + 5
def f2(x): print(x + 5)

nəticə = f1(5) * 2   # ?
nəticə = f2(5) * 2   # ?
```
Niyə `f2` xəta verir? `return` vs `print` fərqi nədir?

**Cavab:**

**`f1(5) * 2` icrası:**

`f1(5)` çağrılanda `x = 5`, `return 5 + 5` → funksiya `10` dəyərini **geri qaytarır**. Bu `10` dəyəri `* 2` ilə çarpılır: `10 * 2 = 20`. `nəticə = 20`.

**`f2(5) * 2` icrası:**

`f2(5)` çağrılanda `x = 5`, `print(5 + 5)` → **ekrana `10` çap olunur**, lakin funksiya heç bir dəyər qaytarmır. Python-da `return` açar sözü olmayan funksiya avtomatik olaraq `None` qaytarır. Buna görə `f2(5)` = `None`. Sonra `None * 2` əməliyyatı aparılmaq istənir, lakin `None` tipli dəyəri ədədlə çarpmaq mümkün deyil → **TypeError: unsupported operand type(s) for *: 'NoneType' and 'int'** xətası alınır.

**`return` açar sözünün rolu:**

`return` funksiyanın hesabladığı nəticəni çağırıcı kontekstə (caller) çıxaran "ixrac qapısı"dır. Bu dəyər tutulub dəyişənə mənimsədilə, başqa əməliyyatlarda istifadə edilə bilər. `print()` isə yalnız ekran çıxışı (I/O əməliyyatı) üçündür — dəyəri yaddaşda saxlamır, geri qaytarmır, yalnız görüntüləyir. Funksiyadan əldə edilən nəticəni sonrakı hesablamalarda istifadə etmək üçün mütləq `return` istifadə olunmalıdır.

---

### Sual 17 (Praktiki)

**Sual:** `data_süzgəci(*args, **kwargs)` funksiyası:
```python
data_süzgəci(10, 'Python', 20.5, 5, portal_icazə=True, admin='Tərlan')
```
`*args` və `**kwargs`-ın içi nə olacaq? `20.5` niyə toplanmır? Tam çıxış nə olacaq?

**Cavab:**

**`*args` nə alır:**

`*args` mövqe arqumentlərini (positional arguments) — ad-ı olmayan arqumentləri — tuple formatında yığır:
```python
args = (10, 'Python', 20.5, 5)
```

**`**kwargs` nə alır:**

`**kwargs` açarlı arqumentləri (keyword arguments) — `ad=dəyər` formatında verilənləri — dictionary formatında yığır:
```python
kwargs = {'portal_icazə': True, 'admin': 'Tərlan'}
```

**`20.5` niyə toplanmır:**

Funksiyanın içindəki `isinstance(parametr, int)` yoxlaması yalnız tam ədədləri (`int` tipi) süzür. `20.5` isə `float` (onluq kəsr) tipidir. `isinstance(20.5, int)` → `False` qaytarır. Buna görə `20.5` `tam_ədədlər_cəmi`-nə əlavə edilmir. `'Python'` sətri `str` tipindədir — o da atlanır.

**Hesablama addımları:**
- `parametr = 10` → `isinstance(10, int)` → True → `tam_ədədlər_cəmi = 0 + 10 = 10`
- `parametr = 'Python'` → `isinstance('Python', int)` → False → atlanır
- `parametr = 20.5` → `isinstance(20.5, int)` → False → atlanır
- `parametr = 5` → `isinstance(5, int)` → True → `tam_ədədlər_cəmi = 10 + 5 = 15`

**Yekun terminal çıxışı:**
```
Tam ədədlərin cəmi: 15
Giriş edən admin: Tərlan
```

`'admin' in kwargs` yoxlaması: `kwargs`-da `'admin'` açarı vardır → True → ikinci `print` icra olunur.

---

## MÖVZu 5: Seaborn və Plotnine Kitabxanaları

---

### Sual 18 (Praktiki)

**Sual:** `sns.scatterplot(data=data, x='displ', y='cty', size='hwy', color='red')` — nöqtələrin ölçüsünü hansı dəyişən təyin edir?

**Cavab:**

Nöqtələrin ölçüsünü (böyüklüyünü) `size='hwy'` parametri təyin edir. Bu parametr Seaborn-a deyir ki, hər nöqtənin ölçüsü `hwy` (avtomagistral yanacaq sərfiyyatı) sütununun dəyəri ilə mütənasib olsun. `hwy` dəyəri böyük olan nöqtələr daha iri, kiçik olan nöqtələr daha xırda çəkiləcək.

`color='red'` parametri isə bütün nöqtələri sabit olaraq qırmızı rəngdə çəkir — bu bir dəyişəndən deyil, sabit rəng dəyərindən götürülmüşdür. Əgər rəng də bir dəyişənə görə dəyişəcəksə, `hue='sütun_adı'` parametrindən istifadə olunur.

---

### Sual 19 (Praktiki)

**Sual:** `sns.histplot(..., multiple='stack')` parametri qrafikin görünüşündə nə dəyişdirir?

**Cavab:**

`multiple='stack'` parametri Seaborn-un histogram funksiyasında **eyni bin (interval) daxilindəki müxtəlif kateqoriyaların bir-birinin üzərinə yığılaraq göstərilməsini** (stacked/üst-üstə) təmin edir.

`multiple` parametri olmadıqda və ya `multiple='layer'` olduqda fərqli kateqoriyalar eyni mövqedə üst-üstə düşür (şəffaflıqla). `multiple='dodge'` halında isə eyni bin daxilindəki çubuqlar yan-yana düzülür.

`multiple='stack'` ilə:
- Hər binde bütün kateqoriyaların çubuqları alt-üst yığılır
- Ümumi hündürlük o bindəki bütün observasiyaların cəmini göstərir
- Hər rəng bir kateqoriyanın bu binkdəki payını vizual olaraq əks etdirir
- Bu format kateqoriyaların həm mütləq, həm də nisbi töhfəsini eyni anda görmək üçün əlverişlidir

---

### Sual 20 (Praktiki)

**Sual:** Seaborn `scatterplot`-da rənglər avtomobil siniflərini (`class`), nöqtə ölçüləri yanacaq sərfiyyatını (`hwy`) göstərmək üçün hansı parametrlər istifadə olunur?

**Cavab:**

Bu görünüşü əldə etmək üçün iki parametrdən istifadə olunur:

**`hue='class'`** — nöqtələrin rəngini (`class`) sütununa görə müəyyən edir. Hər fərqli avtomobil sinfi (SUV, compact, midsize və s.) fərqli rənglə göstərilir. Seaborn avtomatik olaraq rəng palitrasından seçim edib əfsanəni (legend) yaradır.

**`size='hwy'`** — nöqtələrin ölçüsünü `hwy` (avtomagistral yanacaq sərfiyyatı) sütununa görə müəyyən edir. `hwy` dəyəri böyük olan avtomobillər daha böyük nöqtə ilə, kiçik olanlar daha xırda nöqtə ilə göstərilir.

Tam kod nümunəsi:
```python
sns.scatterplot(data=df, x='displ', y='cty', hue='class', size='hwy')
```

---

## MÖVZu 6: Maşın Öyrənməsi Nədir

---

### Sual 21 (Nəzəri)

**Sual:** Maşın Öyrənməsi nədir?

**Cavab:**

Maşın Öyrənməsi (Machine Learning — ML) süni intellektin bir alt sahəsidir. Ənənəvi proqramlaşdırmada insan hər qaydanı açıq şəkildə yazır ("əgər bu, onda o"). Maşın Öyrənməsində isə kompüter sistemi **mövcud məlumatlara (data) əsaslanaraq özü qaydaları aşkar edir** — insan birbaşa qaydaları kodlamır.

Daha texniki izahla: ML alqoritmləri giriş məlumatları (input data) ilə çıxış nəticələri (output) arasındakı əlaqəni öyrənib bir **model** qurur. Bu model sonradan yeni, görülməmiş məlumatlara tətbiq edilərək proqnoz verilir.

Klassik nümunə: E-poçt spam filtri. Minlərlə "spam" və "normal" e-poçt göstərildikdən sonra sistem bu iki sinif arasındakı fərqləri öyrənir. Yeni gələn e-poçtu heç kim "bu spam, bu deyil" deyə kodlamadan sistem özü qərar verir.

---

### Sual 22 (Nəzəri)

**Sual:** Süni İntellekt ilə Maşın Öyrənməsi arasındakı əlaqə haqqında yazın.

**Cavab:**

Süni İntellekt (Artificial Intelligence — AI) insan zəkasını maşınlarda simulyasiya etmənin ümumi sahəsidir. Maşın Öyrənməsi (ML) isə bu geniş sahənin **bir alt sahəsidir**.

Münasibət "hamısını əhatə edən çevrə" şəklindədir:
- **AI** — ən geniş anlayış: istənilən intellektual davranışı maşında gerçəkləşdirmək
- **ML** — AI-nin alt sahəsi: məlumatdan öyrənmə yolu ilə intellektual davranış
- **Dərin Öyrənmə (Deep Learning)** — ML-nin alt sahəsi: çoxqatlı süni neyron şəbəkələri

Bütün ML sistemləri AI sistemidir, lakin bütün AI sistemləri ML deyil. Məsələn, klassik şahmat oynayan proqramlar (qaydaları insan tərəfindən açıq yazılmış) AI-dır, lakin ML deyil. Üzü tanıyan sistem isə həm AI, həm də ML-dir — çünki milyonlarla şəkil üzərindən öyrənib model qurur.

---

### Sual 23 (Nəzəri)

**Sual:** Nəzarətli öyrənmə, Nəzarətsiz öyrənmə və Reinforcement öyrənmə nədir?

**Cavab:**

**Nəzarətli Öyrənmə (Supervised Learning):**

Modelin öyrədilməsi üçün giriş məlumatlarına (X) və onlara uyğun düzgün cavabların (y — etiketlər/labels) verildiyi öyrənmə növüdür. Model "müəllimin nəzarəti altında" öyrənir — hər məlumata uyğun doğru cavabı bilirik. Misal: ev qiymətlərini proqnozlaşdırmaq (giriş: metr, otaq sayı; çıxış: qiymət).

**Nəzarətsiz Öyrənmə (Unsupervised Learning):**

Yalnız giriş məlumatları (X) verilir, düzgün cavablar (etiketlər) yoxdur. Model məlumatlar içindəki gizli strukturları, qruplaşmaları, oxşarlıqları **özü kəşf edir**. Misal: müştəriləri alış-veriş davranışına görə qruplara ayırmaq (klasterləşdirmə). Heç kim əvvəlcədən "bu müştəri qrup 1-dir" demir.

**Reinforcement Öyrənmə (Mükafat Əsaslı Öyrənmə):**

Bir agent (qərar verici) ətraf mühitlə qarşılıqlı əlaqə qurur: hərəkət edir, mühitdən cavab alır (mükafat +, ya cəza −). Məqsəd uzunmüddətli ümumi mükafatı maksimuma çatdırmaqdır. Agent sınaq-xəta yolu ilə optimal strategiyanı öyrənir. Misal: video oyun oynayan AI, robot naviqasiyası, özü idarə olunan avtomobillər.

---

### Sual 24 (Nəzəri)

**Sual:** Nəzarətli öyrənmənin Reqressiya və Klassifikasiya növü haqqında yazın.

**Cavab:**

**Reqressiya (Regression):**

Hədəf dəyişən **kəmiyyət (sayısal, kəsilməz)** bir dəyərdir. Model giriş məlumatlarına əsasən bu kəmiyyətin nə olacağını proqnozlaşdırır.

Nümunələr: ev qiyməti proqnozu, hava temperaturunun gələcək dəyəri, avtomobilin satış qiyməti, bir şirkətin gəlir proqnozu. Nəticə istənilən ədədi dəyər ola bilər: 125000 manat, 23.5 dərəcə, 47800 dollar.

Əsas alqoritmlər: Xətti Reqressiya (Linear Regression), Polinom Reqressiya, Ridge, Lasso, Ağac əsaslı reqressiya modelləri.

**Klassifikasiya (Classification):**

Hədəf dəyişən **kateqorik (diskret, sinif)** bir dəyərdir. Model giriş məlumatlarının hansı sinfə aid olduğunu proqnozlaşdırır.

Nümunələr: e-poçtun spam ya da normal olması (2 sinif — binar), şəkildəki heyvanın it, pişik, ya quş olması (çoxlu sinif), xərçəng şişinin xoşxassəli ya bədxassəli olması.

Əsas alqoritmlər: Logistik Reqressiya, Qərar Ağacı, Random Forest, XGBoost, Naive Bayes, SVM.

---

### Sual 25 (Nəzəri)

**Sual:** Çirkli data nədir? NA/NULL dəyər nədir? Datanın təmizlənməsinin əsas məqsədi nədir?

**Cavab:**

**Çirkli Data (Dirty Data):**

Çirkli data — keyfiyyətsiz, qüsurlu, yanlış və ya istifadəyə hazır olmayan məlumatdır. Çirkliliyə yol açan hallar:
- **Çatışmayan dəyərlər:** bəzi sahələr boş qalmış
- **Dublikatlar:** eyni qeyd bir neçə dəfə daxil edilmiş
- **Format uyğunsuzluqları:** bir sütunda `"2019-03-21"` formatı, digərində `"21/03/2019"` formatı
- **Kənarlaşmalar (outliers):** `yaş = 999` kimi məntiksiz dəyərlər
- **Yanlış məlumat:** `cins = 'kişi'`, amma boyu 210 sm (mümkün, amma şübhəli)

**NA / NULL Dəyər:**

NA (Not Available) və NULL — bir sahədə məlumatın olmadığını bildirən xüsusi işarəçilərdir. Pandas-da `NaN` (Not a Number), Python-da `None` kimi göstərilir. Bu dəyərlər rəqəm deyil, sadəcə "burada məlumat yoxdur" ifadəsidir.

**Datanın Təmizlənməsinin Əsas Məqsədi:**

Maşın öyrənməsi modelləri yalnız tam, düzgün və ardıcıl məlumatlarla düzgün öyrənə bilər. Çirkli məlumat modelin öyrənməsini korlayır — "zibil girər, zibil çıxar" (Garbage In, Garbage Out) prinsipi. Məqsəd: modelin etibarlı proqnozlar verə bilməsi üçün məlumatı standart, tam və keyfiyyətli vəziyyətə gətirmək.

---

### Sual 26 (Nəzəri)

**Sual:** Numerik və Kateqorik dəyişənlərdə NULL dəyərlərlə rəftar necə olmalıdır?

**Cavab:**

**Numerik (Sayısal) Dəyişənlər:**

NULL dəyərlər aşağıdakı üsullardan biri ilə doldurulur:
- **Orta (mean) ilə doldurma:** Məlumat normal paylanıbsa (kənarlaşma yoxdursa). `df['sütun'].fillna(df['sütun'].mean())`
- **Median ilə doldurma:** Kənarlaşmalar varsa orta dəyəri çarpıdığı üçün median daha etibarlıdır.
- **Mode (ən tez-tez rast gəlinən) ilə doldurma:** Nadir hallarda numerik dəyişənlər üçün.
- **Silmə:** Çox az NULL varsa (məsələn, toplam datanın <5%-i), həmin sətirler silinə bilər.
- **Model ilə proqnozlaşdırma:** Mürəkkəb hallarda NULL olan dəyəri digər sütunlara əsasən proqnozlaşdırmaq olar.

**Kateqorik Dəyişənlər:**

- **Mode (ən çox rast gəlinən kateqoriya) ilə doldurma:** Ən sadə üsul. `SimpleImputer(strategy='most_frequent')`
- **Ayrıca kateqoriya yaratmaq:** NULL-ları `'Naməlum'` və ya `'Boş'` kimi ayrı bir sinif kimi göstərmək — bu, bəzən məlumat daşıyır (məsələn, cavab verməmək özü bir siqnaldır).
- **Silmə:** Çox az NULL varsa.

Ümumi qayda: NULL-ları silmədən əvvəl həmişə onların **niyə boş olduğunu** anlamağa çalışın. Bəzən boşluq özü əhəmiyyətli məlumat daşıyır.

---

### Sual 27 (Nəzəri)

**Sual:** Dataya əsaslanan öyrənmə nə deməkdir?

**Cavab:**

Dataya əsaslanan öyrənmə (Data-Driven Learning) — qərar vermə prosesinin insan intuisiyasına, ənənəyə və ya qaydaların əl ilə yazılmasına deyil, **məlumatların analitik olaraq araşdırılmasından çıxan nümunə və əlaqələrə** əsaslandığı yanaşmadır.

Ənənəvi yanaşmada ekspert öz biliyini "əgər müştəri 30 yaşdan böyük və gəliri 3000 manatdan çoxdursa, kredit ver" kimi qaydalar şəklində kodlayır. Dataya əsaslanan yanaşmada isə model minlərlə keçmiş kredit müraciəti və nəticələri oxuyur, özü hansı amillərin vacib olduğunu aşkar edir.

Bu yanaşmanın üstünlükləri:
- Müstəqim insan ekspertizasına olan ehtiyacı azaldır
- Mövcud olmayan ya da ifadə edilməsi çətin olan kompleks əlaqələri tapa bilir
- Məlumat artdıqca model özünü daha da yaxşılaşdıra bilir

Əsas tələbi: kifayət qədər, keyfiyyətli, təmsilçi məlumat olmalıdır. Keyfiyyətsiz məlumat dataya əsaslanan yanaşmanın əleyhinə çevrilir.

---

## MÖVZu 7: Datanın Təmizlənməsi

---

### Sual 28 (Praktiki)

**Sual:** Pandas-da `"2019-03-21"` sətirini tarix tipinə çevirmək üçün hansı funksiya istifadə olunur?

**Cavab:**

`pd.to_datetime()` funksiyası istifadə olunur:

```python
df['tarix_sütunu'] = pd.to_datetime(df['tarix_sütunu'])
# və ya tək dəyər üçün:
tarix = pd.to_datetime("2019-03-21")
```

Bu funksiya sətir (`str`) formatındakı tarix məlumatını Pandas-ın `datetime64` tipinə çevirir. Çevirildikdən sonra `.dt` accessor vasitəsilə il, ay, gün, həftənin günü kimi komponentlərə ayrıca çatmaq mümkün olur: `df['tarix'].dt.year`, `df['tarix'].dt.month`.

Pandas müxtəlif tarix formatlarını avtomatik tanıyır (`YYYY-MM-DD`, `DD/MM/YYYY` və s.), lakin qeyri-standart formatlarda `format` parametri ilə formatı açıq göstərmək tövsiyə olunur: `pd.to_datetime(df['tarix'], format='%d-%m-%Y')`.

---

### Sual 29 (Praktiki)

**Sual:** `df.isna().sum()` əmrinin rolu nədir?

**Cavab:**

Bu əmr iki addımlı əməliyyat yerinə yetirir:

**`df.isna()`** — DataFrame-in hər elementini yoxlayır: element NA (boş, NaN) dirsə `True`, deyilsə `False` yazılır. Nəticə orijinalla eyni ölçüdə bir Boolean DataFrame-dir.

**`.sum()`** — Hər sütun üçün `True` dəyərlərini cəmləyir (Python-da `True` = 1, `False` = 0). Çünki `True` ədədi olaraq `1` sayılır.

**Qaytarılan nəticə:** Hər sütunun adını və o sütundakı NA (boş dəyər) sayını göstərən bir Pandas Series:

```
Ad          0
Yaş         3
Maaş        7
Şəhər       1
dtype: int64
```

Bu, məlumat keyfiyyəti diaqnostikasının ən vacib addımıdır. Hansı sütunlarda nə qədər boşluq olduğunu bir anda görmək imkanı verir, beləliklə hansı sütunlar üçün hansı imputation (doldurma) strategiyasının seçiləcəyi qərara alınır.

---

### Sual 30 (Praktiki)

**Sual:** `df['Expenses'] = df['Expenses'].str.replace(" Dollars", "").astype(float)` — bu sətrin məqsədi nədir?

**Cavab:**

Bu kod sətri 3 ardıcıl addımda icra olunur:

**Addım 1 — `.str.replace(" Dollars", "")`:**
`Expenses` sütunundakı dəyərlər `"150 Dollars"`, `"320 Dollars"` kimi sətir formatında saxlanılıb. `.str.replace(" Dollars", "")` bütün bu dəyərlərdəki `" Dollars"` hissəsini boş sətir ilə əvəzləyir: `"150 Dollars"` → `"150"`, `"320 Dollars"` → `"320"`. Sütun hələ sətir tipindədir.

**Addım 2 — `.astype(float)`:**
Sətir tipindəki `"150"`, `"320"` dəyərlərini rəqəmsal `float` tipinə çevirir: `150.0`, `320.0`. Bu çevirmə olmadan rəqəmsal hesablamalar (cəm, orta, reqressiya) aparıla bilməz — Python sətirləri üzərindəki arifmetik əməliyyatlara icazə vermir.

**Addım 3 — `df['Expenses'] = ...`:**
Nəticəni yenidən eyni sütuna mənimsədir — sütun yerindəcə yenilənir.

**Ümumi məqsəd:** Məlumat bazasına xarici mənbədən idxal zamanı rəqəmsal dəyərlərə vahid adı (`" Dollars"`) birləşdirilmiş formada gəlmişdir. Bu kod həmin sütunu analiz üçün istifadəyə yararlı rəqəmsal formata gətirir.

---

### Sual 31 (Praktiki)

**Sual:** `df.loc[(df['State'].isna()) & (df['City'] == "New York"), 'State'] = "NY"` — bu əmr nə edir?

**Cavab:**

Bu əmr şərtli doldurma (conditional imputation) əməliyyatıdır. Addım-addım:

**Şərt 1:** `df['State'].isna()` — `State` sütunu boş (NA) olan sətirləri tapur → Boolean maskası

**Şərt 2:** `df['City'] == "New York"` — `City` sütununda `"New York"` olan sətirləri tapur → Boolean maskası

**`&` operatoru:** Hər iki şərtin eyni anda doğru olduğu sətirləri seçir — yəni `State`-i boş AND şəhəri "New York" olan sətirler.

**`.loc[şərt, 'State'] = "NY"`:** Bu filtrdən keçən bütün sətirlərin `State` sütununa `"NY"` dəyəri yazılır.

**Əməliyyatın məntiqi:** Məlumat bazasında bəzi qeydlərə `City = "New York"` daxil edilib, lakin `State` sahəsi boş buraxılıb. Bu kod, şəhər "New York" olan amma əyalət boş olan bütün sətirləri avtomatik olaraq `"NY"` ilə doldurur. Bu, kontekstual biliyə əsaslanan ağıllı doldurma üsuludur.

---

### Sual 32 (Praktiki)

**Sual:** IQR metodu ilə kənarlaşmanın yuxarı sərhəddi (upper bound) riyazi olaraq necə hesablanır?

**Cavab:**

**Kvartallar Arası Fərq (IQR) metodunun addımları:**

1. **Q1** (1-ci kvartil, 25-ci persentil) hesablanır — məlumatların aşağı 25%-nin həddidir
2. **Q3** (3-cü kvartil, 75-ci persentil) hesablanır — məlumatların yuxarı 25%-nin həddidir
3. **IQR = Q3 − Q1** — orta 50%-nin genişliyidir

**Yuxarı Sərhəd (Upper Bound) formulu:**

```
Yuxarı Sərhəd = Q3 + 1.5 × IQR
```

**Aşağı Sərhəd (Lower Bound) formulu:**

```
Aşağı Sərhəd = Q1 − 1.5 × IQR
```

Bu iki sərhəddən kənarda qalan istənilən dəyər **kənarlaşma (outlier)** hesab olunur.

**Nümunə:** Q1 = 20, Q3 = 80 olsun.
- IQR = 80 − 20 = 60
- Yuxarı Sərhəd = 80 + 1.5 × 60 = 80 + 90 = **170**
- Aşağı Sərhəd = 20 − 1.5 × 60 = 20 − 90 = **−70**

170-dən böyük və ya -70-dən kiçik hər dəyər kənarlaşmadır.

---

### Sual 33 (Praktiki)

**Sual:** Kənarlaşmaları silmək əvəzinə capping/clipping ilə əvəzləmək üçün Pandas-da hansı məntiq istifadə olunur?

**Cavab:**

Capping (hədd qoyma) üçün Pandas-da iki əsas üsul var:

**1. `.clip()` metodu (ən sadə yol):**
```python
df['sütun'] = df['sütun'].clip(lower=aşağı_sərhəd, upper=yuxarı_sərhəd)
```
`.clip()` aşağı sərhəddən kiçik bütün dəyərləri `aşağı_sərhəd`-ə, yuxarı sərhəddən böyük bütün dəyərləri `yuxarı_sərhəd`-ə bərabərləşdirir.

**2. `.loc[]` ilə şərtli əvəzetmə:**
```python
df.loc[df['sütun'] > yuxarı_sərhəd, 'sütun'] = yuxarı_sərhəd
df.loc[df['sütun'] < aşağı_sərhəd, 'sütun'] = aşağı_sərhəd
```

**Niyə silmək əvəzinə capping istifadə edilir:**
Kənarlaşmaları silmək məlumat itkisinə yol açır — xüsusilə kiçik datasetlərdə bu kritik ola bilər. Capping isə həmin sətri saxlayır, sadəcə həddən kənar dəyəri müəyyən bir limitə "qısır". Bu üsul sətirlərin sayını azaltmadan kənarlaşmanın modelin öyrənməsinə mənfi təsirini azaldır.

---

## MÖVZu 8: Reqressiya Alqoritması

---

### Sual 34 (Nəzəri)

**Sual:** Xətti Reqressiya adətən hansı tip hədəf dəyişənlərini proqnozlaşdırmaq üçün istifadə olunur?

**Cavab:**

Xətti Reqressiya **kəsilməz (continuous), sayısal (numerical)** hədəf dəyişənlərini proqnozlaşdırmaq üçün istifadə olunur. Hədəf dəyişənin müəyyən aralıqda istənilən ədədi qiyməti ala bildiyi hallarda tətbiq edilir.

Klassik nümunələr:
- Ev qiymətinin proqnozlaşdırılması (200,000 ilə 5,000,000 manat arasında istənilən qiymət)
- Temperaturun proqnozlaşdırılması (−20 ilə +50 dərəcə arası)
- Şirkətin gəliri, əmək haqqı, avtomobilin yanacaq sərfiyyatı

Riyazi əsas: `y = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ + ε`

Burada `y` kəsilməz hədəf dəyişəndir, `β` əmsallar modelın öyrəndiyi parametrlərdir. Xətti Reqressiya siniflər (0/1) kimi diskret kateqorik nəticələr üçün uyğun deyil — bunun üçün Logistik Reqressiya istifadə olunur.

---

### Sual 35 (Praktiki)

**Sual:** `SimpleImputer(strategy='most_frequent')` boşluqları necə doldurur?

**Cavab:**

`SimpleImputer(strategy='most_frequent')` hər sütun üçün o sütundakı **ən çox rast gəlinən (mode) dəyəri** hesablayır və o sütundakı bütün NA/NULL dəyərləri həmin mod dəyəri ilə əvəzləyir.

**İşləmə mexanizmi:**

```python
from sklearn.impute import SimpleImputer
imputer = SimpleImputer(strategy='most_frequent')
df_filled = imputer.fit_transform(df)
```

- **`.fit()`** mərhələsində: hər sütunun ən çox rast gəlinən dəyəri hesablanıb yadda saxlanılır
- **`.transform()`** mərhələsinde: saxlanılan mod dəyərləri ilə NA-lar doldurulur

**Nə zaman istifadə edilir:**
- Kateqorik sütunlar üçün ideal seçimdir (məsələn, `'cins'` sütununda ən çox `'kişi'` varsa, boş dəyərlər `'kişi'` ilə doldurulur)
- Sayısal sütunlarda da istifadə oluna bilər, lakin burada `mean` və ya `median` daha çox üstünlük verilir

---

### Sual 36 (Nəzəri)

**Sual:** Reqressiyada "Çoxlu Kollinearlıq" problemi nədir və onu aşkar etmək üçün hansı metrik istifadə olunur?

**Cavab:**

**Çoxlu Kollinearlıq (Multicollinearity):**

Reqressiya modelindəki iki və ya daha çox müstəqil dəyişənin (feature) bir-biri ilə yüksək dərəcədə korrelyasiya etdiyi vəziyyətdir. Məsələn, `boy` və `çəki` dəyişənləri çox vaxt yüksək korrelyasiya göstərir.

**Problemi niyə yaranır:**

Model bu dəyişənlər arasındakı əlaqəni "kimin nəyə töhfə verdiğini" ayırd edə bilmir. Bu vəziyyətdə β əmsalları qeyri-sabit olur — kiçik məlumat dəyişikliyi əmsalların kəskin dəyişməsinə yol açır. Model yorumu (interpretability) çətinləşir.

**Aşkar etmə üçün metrik — VIF (Variance Inflation Factor):**

VIF hər dəyişən üçün hesablanır:
- **VIF = 1:** Kollinearlıq yoxdur
- **VIF = 1–5:** Aşağı, qəbul edilə bilər
- **VIF = 5–10:** Orta, diqqət tələb edir
- **VIF > 10:** Ciddi kollinearlıq — o dəyişəni modeldən çıxarmaq tövsiyə olunur

**Həll üsulları:** Yüksək VIF olan dəyişənlərdən birini silmək, əsas komponent analizi (PCA) tətbiq etmək, ya Ridge reqressiyası istifadə etmək.

---

### Sual 37 (Nəzəri)

**Sual:** One Hot Encoding nədir və niyə tətbiq edilməlidir?

**Cavab:**

**One Hot Encoding (OHE):**

Kateqorik (mətn tipli) dəyişənləri ikili (binary) sayısal formata çevirmə metodudur. Hər kateqoriya üçün ayrıca bir sütun yaradılır; həmin kateqoriya varsa `1`, yoxdursa `0` yazılır.

Nümunə: `rəng` sütununda `['qırmızı', 'mavi', 'yaşıl']` varsa:

| qırmızı | mavi | yaşıl |
|---------|------|--------|
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 0 | 0 | 1 |

**Niyə tətbiq edilməlidir:**

Maşın öyrənməsi alqoritmləri rəqəmsal məlumatlarla işləyir. Kateqorik dəyişənlərə rəqəm (1, 2, 3) mənimsətsək, model bu rəqəmlər arasında yalançı bir iyerarxiya görür: sanki "yaşıl (3) > mavi (2) > qırmızı (1)" kimi. Halbuki rənglər arasında belə bir sıralama yoxdur.

OHE bu problemi aradan qaldırır: hər kateqoriya müstəqil ikili dəyişən kimi göstərilir, aralarında heç bir riyazi üstünlük-aşağılıq münasibəti qalmır.

---

### Sual 38 (Nəzəri)

**Sual:** Stepwise Backward Elimination prosesindo dəyişənlər modeldən hansı meyara görə xaric edilir?

**Cavab:**

**Addım-addım Geriyə Doğru Aradan Qaldırılma (Stepwise Backward Elimination):**

Bu proses aşağıdakı addımlarla aparılır:

1. Bütün dəyişənlər modellə birlikdə başlanır
2. Hər dəyişənin **p-dəyəri (p-value)** yoxlanılır
3. **Ən yüksək p-dəyərinə sahib** olan dəyişən xaric edilir — yəni statistik olaraq ən az əhəmiyyətli olan
4. Model yenidən qurulur, yeni p-dəyərləri yoxlanılır
5. Bütün dəyişənlərin p-dəyəri müəyyən hədd (ənənəvi olaraq α = 0.05) altına düşənə qədər bu proses davam edir

**p-dəyərinin mənası:** Dəyişənin modeldəki əmsalının sıfıra bərabər olma ehtimalını göstərir. P-dəyəri > 0.05 olarsa, o dəyişənin hədəf dəyişənlə statistik əlaqəsi zəifdir — modeldən çıxarılması modelə zərər vermir, hətta onu yaxşılaşdıra bilər (overfitting azalır).

---

### Sual 39 (Nəzəri)

**Sual:** Adjusted R-Squared-ın adi R-Squared-dan üstünlüyü nədir?

**Cavab:**

**Adi R² (R-Squared):**

Modelin hədəf dəyişənin varyasiyasını nə qədər izah etdiyini göstərir (0-dan 1-ə qədər). Problemi: modellə əlaqəsiz, yeni bir dəyişən əlavə edilsə belə R² ya artır, ya da sabit qalır — heç vaxt azalmır. Bu aldadıcıdır.

**Adjusted R² (Düzəldilmiş R-Kvadrat):**

Dəyişən sayını cəzalandırır. Yeni dəyişən modeli **həqiqətən** yaxşılaşdırmırsa, Adjusted R² azalır.

Formul: `Adjusted R² = 1 − [(1 − R²)(n − 1) / (n − k − 1)]`

Burada `n` müşahidə (sətir) sayı, `k` isə dəyişən (sütun) sayıdır.

**Üstünlüyü:** Fərqli sayda dəyişəni olan modellər müqayisə ediləndə Adjusted R² daha ədalətlidir. Dəyişən sayı artdıqda R² süni şəkildə yüksəlir, Adjusted R² isə yalnız həqiqətən faydalı dəyişənlər əlavə olunanda artır. Model seçimində (feature selection) daha etibarlı meyardır.

---

## MÖVZu 9: Klassifikasiya Alqoritması

---

### Sual 40 (Nəzəri)

**Sual:** Logistik Reqressiya modeli hansı tip hədəf dəyişənlər üçün istifadə olunur?

**Cavab:**

Logistik Reqressiya **kateqorik (diskret sinifli) hədəf dəyişənləri** olan problemlər üçün istifadə olunur. Ən çox **binar (ikili) klassifikasiya** problemlərində tətbiq edilir — hədəf dəyişənin yalnız iki mümkün dəyəri olduqda.

Nümunələr:
- E-poçt: spam (1) ya da deyil (0)
- Xəstəlik: var (1) ya da yox (0)
- Kredit: verilsin (1) ya da verilməsin (0)
- Müştəri: çıxacaq (1) ya da qalacaq (0) — churn prediction

Adında "reqressiya" olsa da, Logistik Reqressiya əslində klassifikasiya alqoritmidir. Sigmoid funksiyasını istifadə edərək giriş dəyişənlərini 0 ilə 1 arasındakı ehtimala çevirir. Bu ehtimal müəyyən həddlə (məsələn, 0.5) müqayisə edilərək sinif qərarı verilir. Üç və ya daha çox sinif üçün "Multinomial Logistic Regression" variantı mövcuddur.

---

### Sual 41 (Praktiki)

**Sual:** `data["y"].replace({"yes": 1, "no": 0})` nə edir?

**Cavab:**

Bu kod sətri `data` DataFrame-nin `"y"` sütunundakı mətn (kategorik) dəyərləri sayısal dəyərlərə çevirir:
- `"yes"` olan hər element `1` ilə əvəzlənir
- `"no"` olan hər element `0` ilə əvəzlənir

**Vacib qeyd:** `replace()` metodu orijinal sütunu yerindəcə dəyişdirmir — yeni bir Series qaytarır. Dəyişikliyin qalıcı olması üçün nəticəni sütuna mənimsətmək lazımdır:

```python
data["y"] = data["y"].replace({"yes": 1, "no": 0})
```

Və ya `inplace=True` parametrindən istifadə etmək olar:

```python
data["y"].replace({"yes": 1, "no": 0}, inplace=True)
```

**Məqsəd:** Maşın öyrənməsi alqoritmləri `"yes"`/`"no"` kimi mətn dəyərlərlə işləyə bilmir. Bu çevirmə kateqorik hədəf dəyişənini ikili (binary) sayısal formata keçirir ki, klassifikasiya modeli öyrənə bilsin.

---

### Sual 42 (Nəzəri)

**Sual:** IV (Information Value) metrikasının hesablanmasında məqsəd nədir?

**Cavab:**

**IV (Information Value — Məlumat Dəyəri):**

IV bir dəyişənin hədəf dəyişəni (binary: 0/1) proqnozlaşdırmaq üçün nə qədər faydalı (discriminative power) olduğunu ölçür. Kredit skorlaması, müştəri davranışı analizi kimi binar klassifikasiya problemlərindən əvvəl hansı dəyişənlərin modellə daxil ediləcəyini seçmək üçün istifadə olunur.

**Qərar meyarları:**

| IV Dəyəri | Dəyişənin Gücü |
|-----------|----------------|
| < 0.02 | Faydasız |
| 0.02 – 0.1 | Zəif |
| 0.1 – 0.3 | Orta |
| 0.3 – 0.5 | Güclü |
| > 0.5 | Şübhəli (overfitting riski) |

**Bizə hansı qərarı verməyə kömək edir:**
IV-si çox aşağı olan dəyişənlər modeldən çıxarılır (heç bir ayırt edicilik gücü yoxdur). Çox yüksək olanlar isə məlumat sızıntısı (data leakage) ehtimalına işarə edir. IV, WoE (Weight of Evidence) ilə birlikdə istifadə olunur.

---

### Sual 43 (Praktiki)

**Sual:** XGBClassifier kimi binar klassifikasiya alqoritmlərində `objective` parametrinin dəyəri nə olmalıdır — `reg:squarederror` yoxsa `binary:logistic`?

**Cavab:**

Binar klassifikasiya problemlərində `objective='binary:logistic'` istifadə olunmalıdır.

**Niyə `binary:logistic`:**

- `binary:logistic` hər müşahidə üçün **0 ilə 1 arasında ehtimal** hesablayır (sinif 1-ə aid olma ehtimalı)
- Daxili itki funksiyası (loss function) ikili çarpaz entropi (binary cross-entropy) əsasındadır — bu, klassifikasiya problemlərinin əsas optimallaşdırma meyarıdır
- Nəticəni 0.5 həddilə müqayisə edərək sinif (0 ya da 1) qərarı vermək mümkündür

**Niyə `reg:squarederror` uyğun deyil:**

`reg:squarederror` (kvadrat xəta) **reqressiya** problemləri üçün nəzərdə tutulub — kəsilməz dəyər proqnozlaşdırmaq üçün. Klassifikasiya kontekstindən istifadə etsək, model 0/1 sinif etiketlərini kəsilməz ədədlər kimi proqnozlaşdırmağa çalışar, bu isə məntiqi cəhətdən yanlış və performans baxımından zəif nəticə verər.

---

### Sual 44 (Praktiki)

**Sual:** Naive Bayes (GaussianNB) klassifikatoru hansı əsas ehtimal fərziyyəsinə əsaslanır?

**Cavab:**

**Naive Bayes-in əsas fərziyyəsi: Şərti Müstəqillik (Conditional Independence)**

Naive Bayes hesab edir ki, hər bir dəyişən (feature) digərlərindən **tamamilə müstəqildir** — verilmiş sinif daxilində bir dəyişənin dəyəri digər dəyişənin dəyərinə heç bir təsir göstərmir.

Riyazi ifadəsi: `P(x₁, x₂, ..., xₙ | y) = P(x₁|y) × P(x₂|y) × ... × P(xₙ|y)`

Bu fərziyyə çox vaxt gerçəkliyə uyğun gəlmir — məsələn, evdə otaq sayı ilə evin ölçüsü bir-birilə korrelyasiya edir. Buna baxmayaraq, praktikada Naive Bayes xüsusilə mətn klassifikasiyasında (spam filtri, sentiment analizi) çox yaxşı nəticələr verir, sadəliyi və sürəti ilə ön plana çıxır.

**GaussianNB** xüsusən kəsilməz sayısal dəyişənlər üçün istifadə olunur və hər dəyişənin Normal (Gauss) paylanmasına tabe olduğunu güman edir.

---

## MÖVZu 10: Klasterləşdirmə Alqoritması

---

### Sual 45 (Nəzəri)

**Sual:** K-Means hansı növ Maşın Öyrənməsi metoduna aiddir? Supervised vs Unsupervised fərqi nədir?

**Cavab:**

K-Means **Nəzarətsiz Öyrənmə (Unsupervised Learning)** metoduna aiddir.

**Supervised (Nəzarətli) Öyrənmə:**
Modelin öyrədilməsi üçün `(X, y)` cütlükləri verilir — hər giriş üçün doğru cavab (etiket) bilinir. Model bu etiketlərə əsasən proqnozlaşdırma öyrənir. Nümunə: e-poçtların spam/normal etiketlənib modellə öyrədilməsi.

**Unsupervised (Nəzarətsiz) Öyrənmə:**
Yalnız giriş məlumatları (`X`) verilir, heç bir etiket yoxdur. Model məlumatlar arasındakı gizli strukturları, qruplaşmaları, nümunələri **özü kəşf edir**. K-Means bu məlumatları ən oxşar olanlara görə `k` ədəd qrupa (klastər) ayırır.

**K-Means işləmə prinsipi:**
1. `k` ədəd mərkəz (centroid) təsadüfi seçilir
2. Hər nöqtə özünə ən yaxın mərkəzin klasterinə qoşulur
3. Hər klasterin yeni mərkəzi hesablanır (elementlərin ortası)
4. Mərkəzlər daha dəyişməyənə qədər 2-3 addımlar təkrarlanır

---

### Sual 46 (Nəzəri)

**Sual:** K-Means-də optimal klaster sayını müəyyən etmək üçün Elbow Method istifadə olunur. WCSS nədir? "Dirsək" nöqtəsi nə bildirir?

**Cavab:**

**WCSS (Within-Cluster Sum of Squares — Klaster Daxili Kvadratların Cəmi):**

Hər klasterdəki bütün nöqtələrin öz klaster mərkəzinə olan məsafələrinin karələrinin cəmidir. WCSS klasterin "sıxlığını" ölçür — WCSS nə qədər kiçikdirsə, nöqtələr mərkəzə bir o qədər yaxındır, klaster bir o qədər kompaktdır.

**Elbow Metodu:**

`k = 1, 2, 3, ... n` üçün K-Means tətbiq edilir, hər `k` üçün WCSS hesablanır. `k`-ya qarşı WCSS qrafiki çəkilir:
- Əvvəlcə k artdıqca WCSS kəskin düşür
- Müəyyən nöqtədən sonra azalma sürəti kəskin enir — qrafik "dirsək" şəklini alır
- Bu "dirsək" (kink/elbow) nöqtəsi **optimal klaster sayını** göstərir

**Dirsək nöqtəsinin mənası:**

Bu nöqtədən sonra əlavə klaster əlavə etmək WCSS-ni mənalı şəkildə azaltmır — yəni əlavə klasterlər artıq izahedici deyil, sadəcə datanı lazımsız olaraq parçalayır. Dirsək nöqtəsi deyir: "bu `k` dəyərindən sonra əldə etdiklərin xərcdən az dəyərlidir."

---

## MÖVZu 11: Süni Neyron Şəbəkələri və Dərin Öyrənmə

---

### Sual 47 (Praktiki)

**Sual:** Scikit-learn Pipeline-da həm sayısal miqyaslama, həm də kateqorik kodlaşdırmanı eyni anda aparmaq üçün hansı obyekt istifadə olunur?

**Cavab:**

`ColumnTransformer` obyekti istifadə olunur. Bu, müxtəlif sütun qruplarına müxtəlif transformasiyalar tətbiq etməyə imkan verən güclü alətdir.

```python
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.pipeline import Pipeline

preprocessor = ColumnTransformer(transformers=[
    ('num', StandardScaler(), sayısal_sütunlar),
    ('cat', OneHotEncoder(), kateqorik_sütunlar)
])

pipeline = Pipeline(steps=[
    ('preprocessor', preprocessor),
    ('model', LinearRegression())
])
```

**`ColumnTransformer`-ın üstünlükləri:**
- Sayısal sütunlara `StandardScaler` (miqyaslama), kateqorik sütunlara `OneHotEncoder` (kodlaşdırma) eyni anda tətbiq olunur
- Test datasına eyni transformasiyanın tətbiq edilməsi avtomatik təmin edilir (`fit_transform` vs `transform` ayrımı düzgün idarə olunur)
- Məlumat sızıntısının (data leakage) qarşısı alınır
- Cross-validation ilə birlikdə düzgün işləyir

---

### Sual 48 (Praktiki)

**Sual:** `max_depth` çox böyük seçildikdə Qərar Ağacında hansı problem yaranır?

**Cavab:**

**Həddindən artıq Uyğunlaşma (Overfitting) problemi yaranır.**

`max_depth` parametri Qərar Ağacının neçə səviyyəyə qədər böyüyə biləcəyini məhdudlaşdırır. Bu parametr çox böyük seçildikdə (ya da məhdudlaşdırılmadıqda) ağac özünü **tam olaraq** öyrətmə məlumatlarına uyğunlaşdırır.

**Nə baş verir:**

Ağac öyrətmə datasındakı hər nüansı, hətta təsadüfi gürültünü (noise) belə öyrənir. Öyrətmə setindəki performans demək olar ki mükəmməl olur (R² ≈ 1 ya da accuracy ≈ 100%), lakin model daha əvvəl görmədyi yeni məlumatlar üzərindəki performansı (test seti) kəskin şəkildə pis olur.

**Fəsadları:**

Model realitəni deyil, öyrətmə datasının xüsusiyyətlərini öyrəndiyindən praktikada işə yaramır. Genelləşdirmə (generalization) qabiliyyəti zəifdir. Buna görə `max_depth`, `min_samples_split`, `min_samples_leaf` kimi parametrlərlə ağacı "budamaq" (pruning) lazımdır.

---

### Sual 49 (Nəzəri)

**Sual:** Klassifikasiya və Reqressiya arasındakı əsas fərq nədir?

**Cavab:**

**Reqressiya (Regression):**

Proqnozlaşdırılan nəticə **kəsilməz (continuous) sayısal dəyərdir**. Model bir ədəd çıxarır ki, bu ədəd müəyyən aralıqda istənilən qiymət ala bilər.

Nümunələr: ev qiymətinin proqnozu (450,000 manat), sabahın temperaturu (27.3°C), şirkətin gəliri (2.4 milyon dollar).

Qiymətləndirmə metriklərı: MSE, RMSE, MAE, R².

**Klassifikasiya (Classification):**

Proqnozlaşdırılan nəticə **diskret kateqoriyadır (sinifdir)**. Model bir sinif etiketi çıxarır.

Nümunələr: müştərinin çıxıb-çıxmaması (çıxar/qalmaz), e-poçtun növü (spam/normal), şəkildəki heyvan (it/pişik/quş).

Qiymətləndirmə metriklərı: Accuracy, Precision, Recall, F1-Score, ROC AUC.

**Əsas fərq:** Reqressiyada "nə qədər?" sualı cavablandırılır; Klassifikasiyada "hansı sinifdə?" sualı cavablandırılır. Hədəf dəyişənin tipi (kəsilməz vs. diskret) hansı növün seçiləcəyini müəyyən edir.

---

## MÖVZu 12: Cədvəl Data üçün Dərin Öyrənmə

---

### Sual 50 (Nəzəri)

**Sual:** Klassifikasiya modelinin ehtimallarını 0/1 siniflərinə ayırmaq üçün Optimal Hədd (Threshold) necə müəyyənləşdirilir?

**Cavab:**

Klassifikasiya modeli hər müşahidə üçün `[0, 1]` aralığında bir ehtimal çıxarır. Bu ehtimalı konkret sinifə (0 ya da 1) çevirmək üçün bir hədd (threshold) seçilir. Ənənəvi olaraq `0.5` hədd istifadə olunur, lakin bu hər zaman optimal deyil.

**Optimal Hədd Necə Seçilir:**

Həddin seçimini iş probleminin prioritetləri müəyyən edir:

- **ROC Əyrisinin Yönü:** Müxtəlif həddlər üçün TPR (True Positive Rate) vs FPR (False Positive Rate) qrafiki çəkilir. Hənd "sol yuxarı"ya ən yaxın olan nöqtə optimal hesab olunur.

- **Precision-Recall Balansı:** Yanlış müsbət (False Positive) ilə yanlış mənfi (False Negative) arasındakı xərcləri balanslaşdırmaq:
  - Tibbi diaqnostikada: Xəstəni qaçırmamaq (yüksək Recall) daha vacibdir → hədd aşağı saxlanılır
  - Spam filtrdə: Vacib e-poçtu spam kimi göstərməmək (yüksək Precision) vacibdir → hədd yüksək saxlanılır

- **F1-Score Maksimizasiyası:** Precision və Recall-un harmonik ortasını maksimuma çatdıran hədd seçilir

- **Youden İndeksi:** `Sensitivity + Specificity − 1` ifadəsini maksimuma çatdıran hədd

---

### Sual 51 (Nəzəri)

**Sual:** Balanced Accuracy hansı iki göstəricinin ortasıdır?

**Cavab:**

**Balanced Accuracy (Balanslaşdırılmış Dəqiqlik):**

```
Balanced Accuracy = (Sensitivity + Specificity) / 2
```

- **Sensitivity (Həssaslıq / Recall):** Həqiqi müsbət halların nə qədərinin düzgün müsbət olaraq təsnif edildiyi: `TP / (TP + FN)`

- **Specificity (Spesifiklik):** Həqiqi mənfi halların nə qədərinin düzgün mənfi olaraq təsnif edildiyi: `TN / (TN + FP)`

**Niyə Balanced Accuracy istifadə olunur:**

Adi accuracy balanssız məlumatlarda (imbalanced data) aldadıcıdır. Məsələn, 95% sağlam, 5% xəstə olan datasetdə model hər zaman "sağlam" deyərsə 95% accuracy əldə edir, lakin bir xəstəni belə aşkar etməmiş olur. Balanced Accuracy hər iki sinfin dəqiqliyini bərabər çəkilə ilə hesabladığından bu aldatmanın qarşısını alır.

---

### Sual 52 (Praktiki)

**Sual:** Random Forest və XGBoost-dan hansı ağacları ardıcıl olaraq (əvvəlki ağacın səhvini sonrakı düzəldəcək şəkildə) öyrədir?

**Cavab:**

**XGBoost** ağacları ardıcıl (sequential) olaraq öyrədir.

Bu yanaşma **Boosting** (gücləndirilmə) metoduna əsaslanır:
1. Birinci ağac öyrədilir
2. Birinci ağacın **qalıq xətaları** (residuals) hesablanır
3. İkinci ağac bu xətaları proqnozlaşdırmağa yönəlik öyrədilir
4. Hər yeni ağac əvvəlki ağacların səhvlərini azaltmağa çalışır
5. Bütün ağacların proqnozları toplanır

**Random Forest** isə ağacları **paralel (müstəqil)** olaraq öyrədir (Bagging metodu). Hər ağac məlumatın təsadüfi alt nümunəsindən müstəqil şəkildə öyrənir, ağaclar bir-birindən xəbərsizdir. Son qərar bütün ağacların səs çoxluğu ilə verilir.

---

### Sual 53 (Praktiki)

**Sual:** Random Forest (Bagging) vs XGBoost (Boosting) — ağacları necə formalaşdırır?

**Cavab:**

**Random Forest — Bagging (Bootstrap Aggregating):**

- Hər ağac üçün orijinal datadan **yerinə qoyulmalı nümunə (bootstrap sample)** götürülür
- Hər bölünmə nöqtəsindəki sütunlar **təsadüfi alt çoxluqdan** seçilir
- Bütün ağaclar **eyni vaxtda, müstəqil** olaraq öyrədilir
- Reqressiyada ortalaması, klassifikasiyada səs çoxluğu alınır
- Dispersiyanı (variance) azaltmaq üçün nəzərdə tutulub — fərdi ağacların aşırı uyğunlaşmasını qrupla keçersiz edir

**XGBoost — Gradient Boosting:**

- Ağaclar **ardıcıl** olaraq öyrədilir — hər yeni ağac əvvəlkinin qalıq xətasını öyrənir
- **Qradient azalması (gradient descent)** metodunu itki funksiyasına tətbiq edərək hər addımda itki azaldılır
- Regularizasiya (L1, L2) daxil edərək overfitting-ə qarşı mübarizə aparır
- Yanlılığı (bias) azaltmaq üçün nəzərdə tutulub — yavaş-yavaş daha yaxşı proqnoz əldə edilir
- Adətən daha yüksək proqnoz dəqiqliyi verir, lakin daha uzun öyrənmə vaxtı tələb edir

---

### Sual 54 (Praktiki)

**Sual:** ROC AUC nəyi ölçür? Mükəmməl modeldə bu göstəricinin maksimal dəyəri neçədir?

**Cavab:**

**ROC AUC (Area Under the ROC Curve — ROC Əyrisinin Altındakı Sahə):**

ROC (Receiver Operating Characteristic) əyrisi fərqli hədd dəyərləri üçün `True Positive Rate (Sensitivity)` vs `False Positive Rate (1-Specificity)` cütlüklərini qrafik olaraq göstərir.

**AUC nəyi ölçür:**

Modelin **müsbət və mənfi sinifləri bir-birindən ayırd etmə qabiliyyətini** ölçür. Daha konkret: təsadüfi seçilmiş bir müsbət nümunə ilə təsadüfi seçilmiş bir mənfi nümunəni müqayisə etdikdə modelin müsbət nümunəyə daha yüksək skor verəcəyi ehtimalını göstərir.

**Dəyər aralığı:**

| AUC | Şərh |
|-----|------|
| 1.0 | Mükəmməl model |
| 0.9 – 1.0 | Əla |
| 0.8 – 0.9 | Yaxşı |
| 0.7 – 0.8 | Orta |
| 0.5 | Təsadüfi proqnoz (pulsuz atma) |
| < 0.5 | Tərsə işləyir |

**Maksimal dəyər: `AUC = 1.0`** — model bütün müsbət nümunələrə mənfilərdən daha yüksək skor verir, siniflər mükəmməl ayrılır.

---

## MÖVZu 13: Şəkil Aşkarlanması üçün CNN Alqoritması

---

### Sual 55 (Nəzəri)

**Sual:** Qarışıqlıq Matrisi (Confusion Matrix) nədir? Hansı dörd kateqoriyanı ehtiva edir?

**Cavab:**

**Qarışıqlıq Matrisi:**

Klassifikasiya modelinin proqnozlarını həqiqi dəyərlərlə müqayisə edərək modelin hər sinifdə nə qədər düzgün, nə qədər yanlış proqnoz verdiyini cədvəl formasında göstərən qiymətləndirmə alətidir.

**Dörd əsas kateqoriya (binar klassifikasiya üçün):**

**TP (True Positive — Həqiqi Müsbət):** Model "müsbət" dedi, həqiqətən də müsbətdir. Düzgün müsbət proqnoz. ✓

**TN (True Negative — Həqiqi Mənfi):** Model "mənfi" dedi, həqiqətən də mənfidir. Düzgün mənfi proqnoz. ✓

**FP (False Positive — Yanlış Müsbət / Tip I Xəta):** Model "müsbət" dedi, amma həqiqətdə mənfidir. "Yanlış həyəcan" (false alarm). ✗

**FN (False Negative — Yanlış Mənfi / Tip II Xəta):** Model "mənfi" dedi, amma həqiqətdə müsbətdir. "Buraxılmış aşkarlama" (missed detection). ✗

Bu dörd dəyər Accuracy, Precision, Recall, F1-Score kimi bütün klassifikasiya metriklərinin hesablanmasının əsasını təşkil edir.

---

### Sual 56 (Praktiki)

**Sual:** SMOTE alqoritminin əsas məqsədi və iş prinsipi nədir?

**Cavab:**

**SMOTE (Synthetic Minority Oversampling Technique):**

Balanssız məlumat dəstlərindəki **azlıq sinifini (minority class) süni nümunələrlə artırmaq** üçün istifadə olunan metoddur. Məqsəd: model öyrənilməzdən əvvəl sinifləri balanslaşdırmaq.

**İş prinsipi:**

SMOTE sadəcə mövcud nümunələri kopyalamır — **yeni, süni nümunələr yaradır**:

1. Azlıq sinfindən bir nöqtə seçilir
2. Onun `k` ən yaxın qonşusu (k-nearest neighbors) tapılır
3. Seçilmiş nöqtə ilə onun qonşularından biri arasındakı **xətti interpolasiya** yolu ilə yeni süni nümunə yaradılır
4. Yeni nümunə iki nöqtə arasındakı xətt üzərindəki təsadüfi bir mövqedə yerləşir

**Niyə SMOTE istifadə olunur:**

Sadə çoxaltma (oversampling) eyni nümunəni dəfələrlə kopyalayır — model ezber öyrənir (overfitting). SMOTE isə yeni, müxtəlif nümunələr yaratdığından model azlıq sinifinin ümumi xüsusiyyətlərini öyrənir. Nəticədə Recall artır, balanssız siniflər arasında performans bərabərləşir.

---

### Sual 57 (Praktiki)

**Sual:** `train_test_split(X, y, test_size=0.2)` — `test_size=0.2` nə deməkdir?

**Cavab:**

`test_size=0.2` parametri məlumatın **20%-nin test seti, qalan 80%-nin öyrətmə (train) seti** kimi ayrılmasını bildirir.

**Funksiyası:**

`train_test_split` məlumatı iki hissəyə bölərek modelin:
- **Öyrənməsi** üçün `X_train`, `y_train` (80%)
- **Qiymətləndirilməsi** üçün `X_test`, `y_test` (20%) yaradır

**Niyə test seti ayrılır:**

Model öyrənməsi üçün istifadə edilən məlumatlar üzərindəki performans həqiqi performansı əks etdirmir — model bu məlumatları artıq görüb. Əsl test, modelin daha əvvəl görmediyi yeni məlumatlar üzərindəki davranışıdır. Test seti bu məqsəd üçün öyrənmədən tamamilə kənarda saxlanılır.

Bölmə ənənəvi olaraq 80/20 və ya 70/30 nisbətlərindən istifadə edilir. `random_state` parametri bölmənin təkrarlanabilir olmasını təmin edir.

---

## MÖVZu 14: Təbii Dil Analizi üçün NLP Alqoritması

---

### Sual 58 (Praktiki)

**Sual:** Bayesian Optimization metodunun ənənəvi Grid Search-dən daha səmərəli işləməsinin əsas səbəbini izah edin.

**Cavab:**

**Grid Search-in problemi:**

Grid Search öncədən müəyyən edilmiş bütün hiperparametr kombinasiyalarını **birbaşa sınayır**. Məsələn, 3 parametr üçün hər biri 10 dəyər olarsa, 10³ = 1000 kombinasiya sınanır. Bu çox vaxt aparan, hesablama baxımından bahalı (brute-force) yanaşmadır. Keçmiş sınaqların nəticəsindən öyrənmir.

**Bayesian Optimization-ın üstünlüyü:**

Bayesian Optimization keçmiş sınaqlardan **öyrənərək** növbəti sınanacaq hiperparametr dəyərini ağıllı şəkildə seçir:

1. **Əvvəlki sınaqlar əsasında probabilistik model (surrogate model)** qurulur — hansı hiperparametr dəyərlərinin yaxşı nəticə verəcəyi proqnozlaşdırılır
2. **Əldə etmə funksiyası (acquisition function)** növbəti sınanacaq nöqtəni müəyyən edir: ya ən çox proqnozlaşdırılan yaxşı nəticəyə sahib nöqtəni sına (exploitation), ya da qeyri-müəyyənliyin yüksək olduğu bölgəni araşdır (exploration)
3. Hər yeni sınaq surrogate modeli yeniləyir

**Praktik nəticə:** Grid Search 1000 kombinasiya sınayarkən Bayesian Optimization çox vaxt 50-100 sınaqla eyni (bəzən daha yaxşı) nəticəyə nail olur. Bu, hesablama vaxtını kəskin azaldır.

---

## MÖVZu 15: Zaman Seriyası

---

### Sual 59 (Praktiki)

**Sual:** RMSE MAE-dən xeyli böyük çıxarsa, bu bizə nə siqnal verir?

**Cavab:**

**MAE (Mean Absolute Error):** Bütün xətaların mütləq dəyərlərinin ortasıdır. Hər xəta bərabər çəkilə malikdir.

**RMSE (Root Mean Squared Error):** Xətaların karəsinin ortasının kvadrat kökü. Böyük xətalar karəyə alındığı üçün xüsusilə **ağır cəzalandırılır**.

**RMSE >> MAE olduqda siqnal:**

Bu fərq məlumat bazasında **böyük kənarlaşma xətaları (outlier errors)** olduğuna işarə edir — yəni model bəzi müşahidələri çox kəskin şəkildə yanlış proqnozlaşdırır.

**Konkret izah:** 90 müşahidədə model ±5 vahid xəta edirsə, 10 müşahidədə ±100 vahid xəta edir. MAE bu 10 böyük xətanı digərləri ilə eyni çəkidə tutur, buna görə nisbətən aşağı çıxır. RMSE isə bu 10 xətanı karəyə alaraq 10,000 edir — nəticə kəskin şəkildə yüksəlir.

**Analitik qərar:** RMSE-MAE fərqi böyük olduqda modelin bəzi spesifik bölgələrdə (məsələn, bayram günlərindəki zaman seriyası anomaliyaları, iqtisadi krizis dövrlərindəki qiymət sıçrayışları) çox zəif performans göstərdiyini araşdırmaq lazımdır.

---

### Sual 60 (Praktiki)

**Sual:** Maşın Öyrənməsindəki "Hyperparameter Tuning" prosesinin məqsədi nədir? Bayesian Optimization bu prosesdə nə iş görür?

**Cavab:**

**Hyperparameter Tuning (Hiperparametrlərin Tənzimlənməsi):**

Maşın öyrənməsi modelinin öyrənmə prosesini idarə edən, lakin **özü məlumatdan öyrənilməyən** parametrlərin (hiperparametrlərin) optimallaşdırılması prosesidir.

Nümunələr: Random Forest-də ağac sayı (`n_estimators`), XGBoost-da öyrənmə sürəti (`learning_rate`), neyron şəbəkəsindəki qat sayı, K-Means-dəki `k` dəyəri.

**Məqsəd:** Modelin validasiya setindəki performansını maksimuma çatdıran hiperparametr kombinasiyasını tapmaq — yəni öyrənmə prosesini ən yaxşı şəkildə konfiqurasiya etmək.

**Bayesian Optimization bu prosesdə nə edir:**

Hiperparametr fəzasını ardıcıl olaraq araşdıran **adaptiv axtarış** strategiyasıdır:

- Keçmiş sınaqlardan qurulmuş probabilistik model (Gaussian Process) əsasında növbəti sınanacaq hiperparametr dəyərini seçir
- Artıq yaxşı nəticə verən bölgəni daha dərindən araşdırır (exploitation)
- Hələ sınanmamış bölgəni araşdırır (exploration)
- Hər sınaqdan sonra modeli yeniləyərək getdikcə daha ağıllı qərarlara gəlir

Grid Search-in xaotik, bütün kombinasiyaları sınamaq yanaşmasından fərqli olaraq, Bayesian Optimization az sınaqla yüksək performanslı hiperparametr dəstini tapır.

---

*© 2026 ADNSU — İPFS-B10 Süni İntellekt kursu üzrə final imtahan hazırlıq materialı*
