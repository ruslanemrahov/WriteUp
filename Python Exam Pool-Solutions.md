# Python Final Sualları — Sual & Cavab

> Eyni cavablı suallar birlikdə qruplaşdırılıb.
> Cəmi **15 unikal funksiya** var.

---

## 1. `list_sum(lst)` — Asan
**Mövzular: 1, 3, 5, 7, 9, 11, 13, 15**

**Suallar:**
- Siyahıdakı ədədlərin cəmini qaytarsın.
- `list_sum([4,6,1,3])` → `14`
- `list_sum([5,5,5])` → `15`
- `list_sum([2,4,6])` → `12`
- `list_sum([7,2,5])` → `14`
- `list_sum([1,2,3,4])` → `10`
- `list_sum([5,3,2])` → `10`
- `list_sum([3,6,1])` → `10`

**Cavab:**
```python
def list_sum(lst):
    return sum(lst)
```

---

## 2. `flatten(lst)` — Orta
**Mövzular: 1, 4, 7, 10, 13, 15**

**Suallar:**
- Bir səviyyəli iç-içə siyahını düz siyahıya çevirsin.
- `flatten([[2,3],[7],[1,4]])` → `[2,3,7,1,4]`
- `flatten([[1,2],[3,4],[5]])` → `[1,2,3,4,5]`
- `flatten([1,[2,3],4])` → `[1,2,3,4]`

**Cavab:**
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

## 3. `count_vowels(s)` — Asan
**Mövzular: 1, 4, 6, 8, 10, 12, 14**

**Suallar:**
- Sətirdəki saitlərin sayını qaytarsın (a, e, i, o, u).
- `count_vowels("OpenAI")` → `4`
- `count_vowels("Data")` → `2`
- `count_vowels("Python")` → `1`
- `count_vowels("Open")` → `2`
- `count_vowels("Hello")` → `2`

**Cavab:**
```python
def count_vowels(s):
    return sum(1 for c in s.lower() if c in 'aeiou')
```

---

## 4. `word_freq(text)` — Asan
**Mövzu: 1**

**Sual:**
- Hər sözün neçə dəfə təkrarlandığını göstərən lüğət qaytarsın.
- `word_freq("cat dog cat bird")` → `{'cat':2, 'dog':1, 'bird':1}`

**Cavab:**
```python
def word_freq(text):
    freq = {}
    for word in text.split():
        freq[word] = freq.get(word, 0) + 1
    return freq
```

---

## 5. `find_max(lst)` — Asan
**Mövzular: 2, 3, 6, 9**

**Suallar:**
- Siyahıdakı ən böyük ədədi qaytarsın.
- `find_max([10,3,17,8])` → `17`
- `find_max([-3,-7,-1,-5])` → `-1`
- `find_max([3,8,1,6])` → `8`
- `find_max([12,4,19,6])` → `19`

**Cavab:**
```python
def find_max(lst):
    return max(lst)
```

---

## 6. `split_parity(lst)` — Orta
**Mövzular: 2, 6, 9, 12, 15**

**Suallar:**
- Siyahıdakı ədədləri tək və cüt olaraq ayırsın.
- `split_parity([1,2,3,4,5,6])` → `([1,3,5], [2,4,6])`

**Cavab:**
```python
def split_parity(lst):
    odd = [x for x in lst if x % 2 != 0]
    even = [x for x in lst if x % 2 == 0]
    return (odd, even)
```

---

## 7. `common_words(sent1, sent2)` — Orta
**Mövzular: 2, 7, 10**

**Suallar:**
- İki cümlədə ortaq sözləri tapın.
- `common_words('sun moon', 'moon star')` → `{'moon'}`

**Cavab:**
```python
def common_words(sent1, sent2):
    return set(sent1.split()) & set(sent2.split())
```

---

## 8. `is_palindrome(s)` — Çətin
**Mövzu: 2**

**Sual:**
- String palindromdursa `True`, deyilsə `False` qaytarsın.
- `is_palindrome('Radar')` → `True`
- `is_palindrome('Python')` → `False`

**Cavab:**
```python
def is_palindrome(s):
    s = s.lower()
    return s == s[::-1]
```

---

## 9. `unique_words_by_length(words)` — Orta
**Mövzular: 3, 8, 11, 13**
*(Mövzu 3-də `unique_words(lst)` adı ilə verilir — eyni funksiya)*

**Suallar:**
- Unikal sözləri tapın və uzunluğa görə sırala (qısadan uzuna).
- Giriş: söz siyahısı → Çıxış: unikal sözlər

**Cavab:**
```python
def unique_words_by_length(words):
    return sorted(set(words), key=len)

# Mövzu 3 üçün eyni funksiya unique_words adı ilə:
def unique_words(lst):
    return sorted(set(lst), key=len)
```

---

## 10. `rock_paper_scissors(player1, player2)` — Çətin
**Mövzular: 3, 8, 11, 13**

**Sual:**
- Qalibi müəyyən edin (daş-kağız-qayçı oyunu).
- Giriş: `'rock'`, `'paper'`, `'scissors'` kimi stringlər

**Cavab:**
```python
def rock_paper_scissors(player1, player2):
    if player1 == player2:
        return "Bərabər"
    wins = {
        'rock': 'scissors',
        'scissors': 'paper',
        'paper': 'rock'
    }
    if wins[player1] == player2:
        return "Player 1 qazandı"
    return "Player 2 qazandı"
```

---

## 11. `set_difference(s1, s2)` — Orta
**Mövzular: 4, 8, 12, 14**

**Suallar:**
- Yalnız birinci setdə olan elementləri qaytarın.
- `set_difference({1,2,3}, {2,3,4})` → `{1}`

**Cavab:**
```python
def set_difference(s1, s2):
    return s1 - s2
```

---

## 12. `collatz_sequence(n)` — Çətin
**Mövzular: 4, 7, 10, 14**

**Suallar:**
- N daxil edin; cütdürsə N = N/2, təkdirsə N = 3N+1;
- N = 1 olana qədər davam edin və hər addımı çap edin.
- Nümunə: `collatz_sequence(6)` → çap: 6, 3, 10, 5, 16, 8, 4, 2, 1

**Cavab:**
```python
def collatz_sequence(n):
    while n != 1:
        print(n)
        if n % 2 == 0:
            n = n // 2
        else:
            n = 3 * n + 1
    print(n)  # son addım: 1
```

---

## 13. `fibonacci_sum_even(n)` — Çətin
**Mövzular: 6, 12, 15**

**Sual:**
- İlk N Fibonacci ədədlərini yaradın və cüt elementlərin cəmini qaytarın.
- `fibonacci_sum_even(6)` → `2`
  - *(0,1,1,2,3,5 → cüt olanlar: 0, 2 → cəm: 2)*

**Cavab:**
```python
def fibonacci_sum_even(n):
    fibs = []
    a, b = 0, 1
    for _ in range(n):
        fibs.append(a)
        a, b = b, a + b
    return sum(x for x in fibs if x % 2 == 0)
```

---

## 14. `is_anagram(word1, word2)` — Çətin
**Mövzu: 9**

**Sual:**
- İki sözün anagram olub olmadığını yoxlayın.
- `is_anagram('listen', 'silent')` → `True`
- `is_anagram('hello', 'world')` → `False`

**Cavab:**
```python
def is_anagram(word1, word2):
    return sorted(word1.lower()) == sorted(word2.lower())
```

---

## 15. `find_common_letters(str1, str2)` — Orta
**Mövzular: 11, 14**

**Sual:**
- İki stringdə ortaq hərfləri tapın.
- `find_common_letters('abc', 'bcd')` → `{'b', 'c'}`

**Cavab:**
```python
def find_common_letters(str1, str2):
    return set(str1.lower()) & set(str2.lower())
```

---

## Xülasə cədvəli

| # | Funksiya | Çətilik | Mövzular |
|---|----------|---------|----------|
| 1 | list_sum | Asan | 1,3,5,7,9,11,13,15 |
| 2 | flatten | Orta | 1,4,7,10,13,15 |
| 3 | count_vowels | Asan | 1,4,6,8,10,12,14 |
| 4 | word_freq | Asan | 1 |
| 5 | find_max | Asan | 2,3,6,9 |
| 6 | split_parity | Orta | 2,6,9,12,15 |
| 7 | common_words | Orta | 2,7,10 |
| 8 | is_palindrome | Çətin | 2 |
| 9 | unique_words_by_length | Orta | 3,8,11,13 |
| 10 | rock_paper_scissors | Çətin | 3,8,11,13 |
| 11 | set_difference | Orta | 4,8,12,14 |
| 12 | collatz_sequence | Çətin | 4,7,10,14 |
| 13 | fibonacci_sum_even | Çətin | 6,12,15 |
| 14 | is_anagram | Çətin | 9 |
| 15 | find_common_letters | Orta | 11,14 |
