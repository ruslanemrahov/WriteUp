# Python Mock İmtahan - Cavablar

## 1. Class və Object

### Sual 1

**A: Student class yaradın. Ad və yaş atributlarını göstərən metod yazın.**

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def show(self):
        print(self.name, self.age)
```

**B: Teacher class yaradın. Ad və fənni göstərən metod yazın.**

```python
class Teacher:
    def __init__(self, name, subject):
        self.name = name
        self.subject = subject
    def show(self):
        print(self.name, self.subject)
```

**C: Employee class yaradın. Ad və vəzifəni göstərən metod yazın.**

```python
class Employee:
    def __init__(self, name, position):
        self.name = name
        self.position = position
    def show(self):
        print(self.name, self.position)
```

### Sual 2

**A: Car class yaradın. Marka və model məlumatlarını saxlayın.**

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model
```

**B: Phone class yaradın. Marka və qiyməti saxlayın.**

```python
class Phone:
    def __init__(self, brand, price):
        self.brand = brand
        self.price = price
```

**C: Laptop class yaradın. Marka və RAM məlumatını saxlayın.**

```python
class Laptop:
    def __init__(self, brand, ram):
        self.brand = brand
        self.ram = ram
```

### Sual 3

**A: Book class-ından 3 obyekt yaradın.**

```python
class Book:
    def __init__(self, title):
        self.title = title

b1 = Book("Book1")
b2 = Book("Book2")
b3 = Book("Book3")
```

**B: Student class-ından 5 obyekt yaradın.**

```python
class Student:
    def __init__(self, name):
        self.name = name

students = [Student(f"Student{i}") for i in range(1, 6)]
```

**C: Product class-ından 4 obyekt yaradın.**

```python
class Product:
    def __init__(self, name):
        self.name = name

products = [Product(f"Product{i}") for i in range(1, 5)]
```

### Sual 4

**A: Person class-ında introduce() metodu yaradın.**

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    def introduce(self):
        print(f"My name is {self.name}, I am {self.age}")
```

**B: Teacher class-ında info() metodu yaradın.**

```python
class Teacher:
    def __init__(self, name, subject):
        self.name = name
        self.subject = subject
    def info(self):
        print(f"{self.name} teaches {self.subject}")
```

**C: Employee class-ında display() metodu yaradın.**

```python
class Employee:
    def __init__(self, name, position):
        self.name = name
        self.position = position
    def display(self):
        print(f"{self.name} - {self.position}")
```

### Sual 5

**A: Rectangle class-ında sahəni hesablayın.**

```python
class Rectangle:
    def __init__(self, w, h):
        self.w = w
        self.h = h
    def area(self):
        return self.w * self.h
```

**B: Triangle class-ında sahəni hesablayın.**

```python
class Triangle:
    def __init__(self, base, height):
        self.base = base
        self.height = height
    def area(self):
        return 0.5 * self.base * self.height
```

**C: Circle class-ında sahəni hesablayın.**

```python
import math

class Circle:
    def __init__(self, r):
        self.r = r
    def area(self):
        return math.pi * self.r ** 2
```


## 2. init və self

### Sual 6

**A: Employee class-ında ad və maaşı constructor vasitəsilə qəbul edin.**

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary
```

**B: Student class-ında ad və qrup məlumatını constructor vasitəsilə qəbul edin.**

```python
class Student:
    def __init__(self, name, group):
        self.name = name
        self.group = group
```

**C: Book class-ında kitab adı və müəllifi constructor vasitəsilə qəbul edin.**

```python
class Book:
    def __init__(self, title, author):
        self.title = title
        self.author = author
```

### Sual 7

**A: Laptop class-ında self istifadə edin.**

```python
class Laptop:
    def __init__(self, brand, ram):
        self.brand = brand
        self.ram = ram
    def show(self):
        print(self.brand, self.ram)
```

**B: Car class-ında self istifadə edin.**

```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model
    def show(self):
        print(self.brand, self.model)
```

**C: Phone class-ında self istifadə edin.**

```python
class Phone:
    def __init__(self, brand, price):
        self.brand = brand
        self.price = price
    def show(self):
        print(self.brand, self.price)
```

### Sual 8

**A: Animal class-ında ad atributu yaradın.**

```python
class Animal:
    def __init__(self, name):
        self.name = name
```

**B: City class-ında şəhər adı atributu yaradın.**

```python
class City:
    def __init__(self, name):
        self.name = name
```

**C: Movie class-ında film adı atributu yaradın.**

```python
class Movie:
    def __init__(self, name):
        self.name = name
```

### Sual 9

**A: Course class-ında kurs adı və kredit sayı saxlayın.**

```python
class Course:
    def __init__(self, name, credits):
        self.name = name
        self.credits = credits
```

**B: Subject class-ında fənn adı və saat sayı saxlayın.**

```python
class Subject:
    def __init__(self, name, hours):
        self.name = name
        self.hours = hours
```

**C: Seminar class-ında mövzu və müddət saxlayın.**

```python
class Seminar:
    def __init__(self, topic, duration):
        self.topic = topic
        self.duration = duration
```

### Sual 10

**A: Phone class-ında marka və qiyməti saxlayın.**

```python
class Phone:
    def __init__(self, brand, price):
        self.brand = brand
        self.price = price
```

**B: Car class-ında marka və sürəti saxlayın.**

```python
class Car:
    def __init__(self, brand, speed):
        self.brand = brand
        self.speed = speed
```

**C: Product class-ında ad və qiyməti saxlayın.**

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price
```


## 3. Functions

### Sual 11

**A: İki ədədin cəmini hesablayan funksiya yazın.**

```python
def add(a, b):
    return a + b
```

**B: Üç ədədin cəmini hesablayan funksiya yazın.**

```python
def add(a, b, c):
    return a + b + c
```

**C: Siyahıdakı bütün elementlərin cəmini hesablayan funksiya yazın.**

```python
def total(lst):
    return sum(lst)
```

### Sual 12

**A: Ədədin kvadratını hesablayın.**

```python
def square(n):
    return n ** 2
```

**B: Ədədin kubunu hesablayın.**

```python
def cube(n):
    return n ** 3
```

**C: Ədədin 4-cü dərəcəsini hesablayın.**

```python
def power4(n):
    return n ** 4
```

### Sual 13

**A: Siyahıdakı ən böyük elementi tapın.**

```python
def find_max(lst):
    return max(lst)
```

**B: Siyahıdakı ən kiçik elementi tapın.**

```python
def find_min(lst):
    return min(lst)
```

**C: Siyahının ortalamasını hesablayın.**

```python
def average(lst):
    return sum(lst) / len(lst)
```

### Sual 14

**A: String-i tərsinə çevirin.**

```python
def reverse_str(s):
    return s[::-1]
```

**B: String-dəki saitlərin sayını tapın.**

```python
def count_vowels(s):
    return sum(1 for c in s.lower() if c in "aeiou")
```

**C: String-dəki sözlərin sayını tapın.**

```python
def count_words(s):
    return len(s.split())
```

### Sual 15

**A: Faktorial hesablayan funksiya yazın.**

```python
def factorial(n):
    return 1 if n <= 1 else n * factorial(n - 1)
```

**B: Fibonacci seriyasının n-ci elementini tapın.**

```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a
```

**C: Ədədin sadə olub-olmadığını yoxlayın.**

```python
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True
```


## 4. Inheritance

### Sual 31

**A: Animal → Dog**

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def bark(self):
        print(f"{self.name} says Woof")
```

**B: Vehicle → Car**

```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

class Car(Vehicle):
    def drive(self):
        print(f"{self.brand} is driving")
```

**C: Person → Student**

```python
class Person:
    def __init__(self, name):
        self.name = name

class Student(Person):
    def study(self):
        print(f"{self.name} is studying")
```

### Sual 32

**A: Person → Teacher**

```python
class Person:
    def __init__(self, name):
        self.name = name

class Teacher(Person):
    def teach(self):
        print(f"{self.name} is teaching")
```

**B: Employee → Manager**

```python
class Employee:
    def __init__(self, name):
        self.name = name

class Manager(Employee):
    def manage(self):
        print(f"{self.name} is managing")
```

**C: User → Admin**

```python
class User:
    def __init__(self, name):
        self.name = name

class Admin(User):
    def manage_users(self):
        print(f"{self.name} manages users")
```

### Sual 33

**A: Vehicle → Car**

```python
class Vehicle:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

class Car(Vehicle):
    pass
```

**B: Shape → Rectangle**

```python
class Shape:
    def __init__(self, name):
        self.name = name

class Rectangle(Shape):
    def __init__(self, name, w, h):
        super().__init__(name)
        self.w = w
        self.h = h
```

**C: Animal → Cat**

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Cat(Animal):
    def meow(self):
        print(f"{self.name} says Meow")
```

### Sual 34

**A: Employee → Manager**

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

class Manager(Employee):
    def __init__(self, name, salary, team):
        super().__init__(name, salary)
        self.team = team
```

**B: Teacher → HeadTeacher**

```python
class Teacher:
    def __init__(self, name, subject):
        self.name = name
        self.subject = subject

class HeadTeacher(Teacher):
    def __init__(self, name, subject, department):
        super().__init__(name, subject)
        self.department = department
```

**C: Student → GraduateStudent**

```python
class Student:
    def __init__(self, name, group):
        self.name = name
        self.group = group

class GraduateStudent(Student):
    def __init__(self, name, group, thesis):
        super().__init__(name, group)
        self.thesis = thesis
```

### Sual 35

**A: Parent class metodunu çağırın.**

```python
class Parent:
    def greet(self):
        print("Hello from Parent")

class Child(Parent):
    def greet(self):
        Parent.greet(self)
        print("Hello from Child")
```

**B: super() istifadə edin.**

```python
class Parent:
    def greet(self):
        print("Hello from Parent")

class Child(Parent):
    def greet(self):
        super().greet()
        print("Hello from Child")
```

**C: Parent constructorunu çağırın.**

```python
class Parent:
    def __init__(self, name):
        self.name = name

class Child(Parent):
    def __init__(self, name, age):
        super().__init__(name)
        self.age = age
```


## 5. Polymorphism

### Sual 36

**A: Cat və Dog üçün sound()**

```python
class Cat:
    def sound(self):
        print("Meow")

class Dog:
    def sound(self):
        print("Woof")

for a in [Cat(), Dog()]:
    a.sound()
```

**B: Car və Bike üçün move()**

```python
class Car:
    def move(self):
        print("Car is driving")

class Bike:
    def move(self):
        print("Bike is riding")

for v in [Car(), Bike()]:
    v.move()
```

**C: Bird və Plane üçün fly()**

```python
class Bird:
    def fly(self):
        print("Bird is flying")

class Plane:
    def fly(self):
        print("Plane is flying")

for x in [Bird(), Plane()]:
    x.fly()
```

### Sual 37

**A: Rectangle və Circle üçün area()**

```python
import math

class Rectangle:
    def __init__(self, w, h):
        self.w, self.h = w, h
    def area(self):
        return self.w * self.h

class Circle:
    def __init__(self, r):
        self.r = r
    def area(self):
        return math.pi * self.r ** 2

for shape in [Rectangle(3, 4), Circle(5)]:
    print(shape.area())
```

**B: Square və Triangle üçün area()**

```python
class Square:
    def __init__(self, side):
        self.side = side
    def area(self):
        return self.side ** 2

class Triangle:
    def __init__(self, base, height):
        self.base, self.height = base, height
    def area(self):
        return 0.5 * self.base * self.height

for shape in [Square(4), Triangle(3, 6)]:
    print(shape.area())
```

**C: Parallelogram və Circle üçün area()**

```python
import math

class Parallelogram:
    def __init__(self, base, height):
        self.base, self.height = base, height
    def area(self):
        return self.base * self.height

class Circle:
    def __init__(self, r):
        self.r = r
    def area(self):
        return math.pi * self.r ** 2

for shape in [Parallelogram(5, 3), Circle(2)]:
    print(shape.area())
```

### Sual 38

**A: Bird, Plane, Drone → move()**

```python
class Bird:
    def move(self):
        print("Bird flies")

class Plane:
    def move(self):
        print("Plane flies")

class Drone:
    def move(self):
        print("Drone flies")

for x in [Bird(), Plane(), Drone()]:
    x.move()
```

**B: Fish, Boat, Submarine → move()**

```python
class Fish:
    def move(self):
        print("Fish swims")

class Boat:
    def move(self):
        print("Boat sails")

class Submarine:
    def move(self):
        print("Submarine dives")

for x in [Fish(), Boat(), Submarine()]:
    x.move()
```

**C: Car, Train, Bicycle → move()**

```python
class Car:
    def move(self):
        print("Car drives")

class Train:
    def move(self):
        print("Train runs")

class Bicycle:
    def move(self):
        print("Bicycle rides")

for x in [Car(), Train(), Bicycle()]:
    x.move()
```


## 6. Encapsulation

### Sual 41

**A: Maaşı private edin.**

```python
class Employee:
    def __init__(self, salary):
        self.__salary = salary
```

**B: Balansı private edin.**

```python
class Account:
    def __init__(self, balance):
        self.__balance = balance
```

**C: Qiyməti private edin.**

```python
class Product:
    def __init__(self, price):
        self.__price = price
```

### Sual 42

**A: Getter metodu yazın.**

```python
class Employee:
    def __init__(self, salary):
        self.__salary = salary
    def get_salary(self):
        return self.__salary
```

**B: Private atributu oxuyan metod yazın.**

```python
class Account:
    def __init__(self, balance):
        self.__balance = balance
    def get_balance(self):
        return self.__balance
```

**C: Balansı göstərən metod yazın.**

```python
class Account:
    def __init__(self, balance):
        self.__balance = balance
    def show_balance(self):
        print(self.__balance)
```

### Sual 43

**A: Setter metodu yazın.**

```python
class Employee:
    def __init__(self, salary):
        self.__salary = salary
    def set_salary(self, salary):
        self.__salary = salary
```

**B: Maaşı yeniləyən metod yazın.**

```python
class Employee:
    def __init__(self, salary):
        self.__salary = salary
    def update_salary(self, amount):
        self.__salary += amount
```

**C: Qiyməti dəyişən metod yazın.**

```python
class Product:
    def __init__(self, price):
        self.__price = price
    def change_price(self, new_price):
        self.__price = new_price
```


## 7. *args və **kwargs

### Sual 46

**A: *args ilə cəm hesablayın.**

```python
def total(*args):
    return sum(args)
```

**B: *args ilə hasil hesablayın.**

```python
def product(*args):
    result = 1
    for n in args:
        result *= n
    return result
```

**C: *args ilə orta qiymət hesablayın.**

```python
def average(*args):
    return sum(args) / len(args)
```

### Sual 47

**A: *args ilə maksimum elementi tapın.**

```python
def find_max(*args):
    return max(args)
```

**B: *args ilə minimum elementi tapın.**

```python
def find_min(*args):
    return min(args)
```

**C: *args ilə element sayını tapın.**

```python
def count(*args):
    return len(args)
```

### Sual 48

**A: **kwargs ilə istifadəçi məlumatlarını çap edin.**

```python
def print_user(**kwargs):
    for k, v in kwargs.items():
        print(k, ":", v)
```

**B: **kwargs ilə məhsul məlumatlarını çap edin.**

```python
def print_product(**kwargs):
    for k, v in kwargs.items():
        print(k, ":", v)
```

**C: **kwargs ilə tələbə məlumatlarını çap edin.**

```python
def print_student(**kwargs):
    for k, v in kwargs.items():
        print(k, ":", v)
```


## 8. File Handling

### Sual 56

**A: Fayldakı sözlərin sayını hesablayın.**

```python
with open("file.txt") as f:
    print(len(f.read().split()))
```

**B: Fayldakı simvolların sayını hesablayın.**

```python
with open("file.txt") as f:
    print(len(f.read()))
```

**C: Fayldakı sətirlərin sayını hesablayın.**

```python
with open("file.txt") as f:
    print(len(f.readlines()))
```

### Sual 57

**A: Müəyyən sözün neçə dəfə keçdiyini tapın.**

```python
with open("file.txt") as f:
    print(f.read().split().count("word"))
```

**B: Müəyyən hərfin neçə dəfə keçdiyini tapın.**

```python
with open("file.txt") as f:
    print(f.read().count("a"))
```

**C: Müəyyən sətrin neçə dəfə keçdiyini tapın.**

```python
with open("file.txt") as f:
    lines = f.readlines()
print(lines.count("target line\n"))
```

### Sual 58

**A: İki faylı birləşdirin.**

```python
with open("out.txt", "w") as out:
    for fname in ["a.txt", "b.txt"]:
        with open(fname) as f:
            out.write(f.read())
```

**B: Üç faylı birləşdirin.**

```python
with open("out.txt", "w") as out:
    for fname in ["a.txt", "b.txt", "c.txt"]:
        with open(fname) as f:
            out.write(f.read())
```

**C: Faylları yeni fayla köçürün.**

```python
with open("source.txt") as src, open("new.txt", "w") as dst:
    dst.write(src.read())
```

### Sual 59

**A: CSV formatında tələbə məlumatlarını fayla yazın.**

```python
import csv

students = [["Ali", 20], ["Vali", 21]]
with open("students.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["name", "age"])
    writer.writerows(students)
```

**B: CSV formatında məhsul məlumatlarını fayla yazın.**

```python
import csv

products = [["Phone", 500], ["Laptop", 1000]]
with open("products.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["name", "price"])
    writer.writerows(products)
```

**C: CSV formatında işçi məlumatlarını fayla yazın.**

```python
import csv

employees = [["Ali", 1000], ["Vali", 1500]]
with open("employees.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["name", "salary"])
    writer.writerows(employees)
```

### Sual 60

**A: Fayldakı sözləri əlifba sırası ilə düzün.**

```python
with open("file.txt") as f:
    words = sorted(f.read().split())
print(words)
```

**B: Fayldakı sətirləri əlifba sırası ilə düzün.**

```python
with open("file.txt") as f:
    lines = sorted(f.readlines())
print(lines)
```

**C: Fayldakı adları əlifba sırası ilə düzün.**

```python
with open("file.txt") as f:
    names = sorted(line.strip() for line in f)
print(names)
```


## 9. OOP Kompleks Tapşırıqlar

### Sual 61

**A: Tələbə idarəetmə sistemi yaradın (əlavə et, sil, göstər).**

```python
class StudentSystem:
    def __init__(self):
        self.students = []
    def add(self, name):
        self.students.append(name)
    def remove(self, name):
        self.students.remove(name)
    def show(self):
        print(self.students)
```

**B: Müəllim idarəetmə sistemi yaradın (əlavə et, sil, göstər).**

```python
class TeacherSystem:
    def __init__(self):
        self.teachers = []
    def add(self, name):
        self.teachers.append(name)
    def remove(self, name):
        self.teachers.remove(name)
    def show(self):
        print(self.teachers)
```

**C: İşçi idarəetmə sistemi yaradın (əlavə et, sil, göstər).**

```python
class EmployeeSystem:
    def __init__(self):
        self.employees = []
    def add(self, name):
        self.employees.append(name)
    def remove(self, name):
        self.employees.remove(name)
    def show(self):
        print(self.employees)
```

### Sual 62

**A: Kitabxana idarəetmə sistemi yaradın.**

```python
class Library:
    def __init__(self):
        self.books = []
    def add_book(self, title):
        self.books.append(title)
    def remove_book(self, title):
        self.books.remove(title)
    def show_books(self):
        print(self.books)
```

**B: Film arxivi idarəetmə sistemi yaradın.**

```python
class FilmArchive:
    def __init__(self):
        self.films = []
    def add_film(self, title):
        self.films.append(title)
    def remove_film(self, title):
        self.films.remove(title)
    def show_films(self):
        print(self.films)
```

**C: Musiqi kolleksiyası idarəetmə sistemi yaradın.**

```python
class MusicCollection:
    def __init__(self):
        self.songs = []
    def add_song(self, title):
        self.songs.append(title)
    def remove_song(self, title):
        self.songs.remove(title)
    def show_songs(self):
        print(self.songs)
```

### Sual 63

**A: Bank hesabı sistemi yaradın (depozit, çıxarış, balans).**

```python
class BankAccount:
    def __init__(self, balance=0):
        self.balance = balance
    def deposit(self, amount):
        self.balance += amount
    def withdraw(self, amount):
        self.balance -= amount
    def show_balance(self):
        print(self.balance)
```

**B: Elektron pul kisəsi sistemi yaradın (əlavə et, xərclə, balans).**

```python
class EWallet:
    def __init__(self, balance=0):
        self.balance = balance
    def add_funds(self, amount):
        self.balance += amount
    def spend(self, amount):
        self.balance -= amount
    def show_balance(self):
        print(self.balance)
```

**C: Mağaza kassası sistemi yaradın (ödəniş, geri qaytarma, balans).**

```python
class Cashier:
    def __init__(self, balance=0):
        self.balance = balance
    def pay(self, amount):
        self.balance += amount
    def refund(self, amount):
        self.balance -= amount
    def show_balance(self):
        print(self.balance)
```

### Sual 64

**A: Məhsul və sifariş sistemi yaradın.**

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class Order:
    def __init__(self):
        self.items = []
    def add_item(self, product):
        self.items.append(product)
    def total(self):
        return sum(p.price for p in self.items)
```

**B: Restoran menyu və sifariş sistemi yaradın.**

```python
class MenuItem:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class Order:
    def __init__(self):
        self.items = []
    def add_item(self, item):
        self.items.append(item)
    def total(self):
        return sum(i.price for i in self.items)
```

**C: Onlayn mağaza və səbət sistemi yaradın.**

```python
class Item:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class Cart:
    def __init__(self):
        self.items = []
    def add_item(self, item):
        self.items.append(item)
    def total(self):
        return sum(i.price for i in self.items)
```

### Sual 65

**A: İşçi idarəetmə sistemi hazırlayın.**

```python
class EmployeeManagement:
    def __init__(self):
        self.employees = {}
    def add(self, emp_id, name):
        self.employees[emp_id] = name
    def remove(self, emp_id):
        del self.employees[emp_id]
    def show(self):
        print(self.employees)
```

**B: Tələbə qeydiyyat sistemi hazırlayın.**

```python
class StudentRegistration:
    def __init__(self):
        self.students = {}
    def register(self, student_id, name):
        self.students[student_id] = name
    def unregister(self, student_id):
        del self.students[student_id]
    def show(self):
        print(self.students)
```

**C: Kurs iştirakçıları idarəetmə sistemi hazırlayın.**

```python
class CourseParticipants:
    def __init__(self):
        self.participants = {}
    def add(self, participant_id, name):
        self.participants[participant_id] = name
    def remove(self, participant_id):
        del self.participants[participant_id]
    def show(self):
        print(self.participants)
```


## 10. Qarışıq Çətin Tapşırıqlar

### Sual 66

**A: Mirasalma və encapsulation istifadə edərək məktəb sistemi yaradın.**

```python
class Person:
    def __init__(self, name):
        self._name = name

class Teacher(Person):
    def __init__(self, name, subject):
        super().__init__(name)
        self.__subject = subject
    def get_subject(self):
        return self.__subject

class Student(Person):
    def __init__(self, name, grade):
        super().__init__(name)
        self.__grade = grade
    def get_grade(self):
        return self.__grade
```

**B: Mirasalma və encapsulation istifadə edərək xəstəxana sistemi yaradın.**

```python
class Person:
    def __init__(self, name):
        self._name = name

class Doctor(Person):
    def __init__(self, name, specialty):
        super().__init__(name)
        self.__specialty = specialty
    def get_specialty(self):
        return self.__specialty

class Patient(Person):
    def __init__(self, name, disease):
        super().__init__(name)
        self.__disease = disease
    def get_disease(self):
        return self.__disease
```

**C: Mirasalma və encapsulation istifadə edərək şirkət sistemi yaradın.**

```python
class Person:
    def __init__(self, name):
        self._name = name

class Manager(Person):
    def __init__(self, name, department):
        super().__init__(name)
        self.__department = department
    def get_department(self):
        return self.__department

class Employee(Person):
    def __init__(self, name, salary):
        super().__init__(name)
        self.__salary = salary
    def get_salary(self):
        return self.__salary
```

### Sual 67

**A: Polymorphism istifadə edərək ödəniş sistemi yaradın (Cash, Card, Transfer).**

```python
class Payment:
    def pay(self, amount):
        pass

class Cash(Payment):
    def pay(self, amount):
        print(f"Paid {amount} with cash")

class Card(Payment):
    def pay(self, amount):
        print(f"Paid {amount} with card")

class Transfer(Payment):
    def pay(self, amount):
        print(f"Paid {amount} with transfer")
```

**B: Polymorphism istifadə edərək çatdırılma sistemi yaradın (Courier, Pickup, Drone).**

```python
class Delivery:
    def deliver(self):
        pass

class Courier(Delivery):
    def deliver(self):
        print("Delivered by courier")

class Pickup(Delivery):
    def deliver(self):
        print("Delivered by pickup")

class Drone(Delivery):
    def deliver(self):
        print("Delivered by drone")
```

**C: Polymorphism istifadə edərək nəqliyyat sistemi yaradın (Car, Bus, Train).**

```python
class Transport:
    def move(self):
        pass

class Car(Transport):
    def move(self):
        print("Car moves on road")

class Bus(Transport):
    def move(self):
        print("Bus moves on route")

class Train(Transport):
    def move(self):
        print("Train moves on rails")
```

### Sual 68

**A: Fayldan tələbə məlumatlarını oxuyub obyektlərə çevirin.**

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

students = []
with open("students.txt") as f:
    for line in f:
        name, age = line.strip().split(",")
        students.append(Student(name, int(age)))
```

**B: Fayldan işçi məlumatlarını oxuyub obyektlərə çevirin.**

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

employees = []
with open("employees.txt") as f:
    for line in f:
        name, salary = line.strip().split(",")
        employees.append(Employee(name, int(salary)))
```

**C: Fayldan məhsul məlumatlarını oxuyub obyektlərə çevirin.**

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

products = []
with open("products.txt") as f:
    for line in f:
        name, price = line.strip().split(",")
        products.append(Product(name, float(price)))
```

### Sual 69

**A: Inner class və class method istifadə edərək universitet sistemi hazırlayın.**

```python
class University:
    count = 0
    def __init__(self, name):
        self.name = name
        University.count += 1

    class Department:
        def __init__(self, name):
            self.name = name

    @classmethod
    def total(cls):
        return cls.count
```

**B: Inner class və class method istifadə edərək şirkət sistemi hazırlayın.**

```python
class Company:
    count = 0
    def __init__(self, name):
        self.name = name
        Company.count += 1

    class Department:
        def __init__(self, name):
            self.name = name

    @classmethod
    def total(cls):
        return cls.count
```

**C: Inner class və class method istifadə edərək kitabxana sistemi hazırlayın.**

```python
class Library:
    count = 0
    def __init__(self, name):
        self.name = name
        Library.count += 1

    class Section:
        def __init__(self, name):
            self.name = name

    @classmethod
    def total(cls):
        return cls.count
```

### Sual 70

**A: OOP prinsiplərinin hamısından istifadə edərək Universitet İdarəetmə Sistemi hazırlayın.**

```python
class Person:
    def __init__(self, name):
        self._name = name

class Student(Person):
    def __init__(self, name, gpa):
        super().__init__(name)
        self.__gpa = gpa
    def get_gpa(self):
        return self.__gpa

class Teacher(Person):
    def __init__(self, name, subject):
        super().__init__(name)
        self.subject = subject

class University:
    def __init__(self):
        self.students = []
        self.teachers = []
    def add_student(self, student):
        self.students.append(student)
    def add_teacher(self, teacher):
        self.teachers.append(teacher)
```

**B: OOP prinsiplərinin hamısından istifadə edərək Xəstəxana İdarəetmə Sistemi hazırlayın.**

```python
class Person:
    def __init__(self, name):
        self._name = name

class Patient(Person):
    def __init__(self, name, disease):
        super().__init__(name)
        self.__disease = disease
    def get_disease(self):
        return self.__disease

class Doctor(Person):
    def __init__(self, name, specialty):
        super().__init__(name)
        self.specialty = specialty

class Hospital:
    def __init__(self):
        self.patients = []
        self.doctors = []
    def add_patient(self, patient):
        self.patients.append(patient)
    def add_doctor(self, doctor):
        self.doctors.append(doctor)
```

**C: OOP prinsiplərinin hamısından istifadə edərək Şirkət İdarəetmə Sistemi hazırlayın.**

```python
class Person:
    def __init__(self, name):
        self._name = name

class Employee(Person):
    def __init__(self, name, salary):
        super().__init__(name)
        self.__salary = salary
    def get_salary(self):
        return self.__salary

class Manager(Person):
    def __init__(self, name, department):
        super().__init__(name)
        self.department = department

class Company:
    def __init__(self):
        self.employees = []
        self.managers = []
    def add_employee(self, emp):
        self.employees.append(emp)
    def add_manager(self, mgr):
        self.managers.append(mgr)
```


## 11. Bonus Çətin Suallar

### Sual 71

**A: JSON faylından tələbə məlumatlarını oxuyaraq obyektlər yaradın.**

```python
import json

class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

with open("students.json") as f:
    data = json.load(f)

students = [Student(s["name"], s["age"]) for s in data]
```

**B: JSON faylından məhsul məlumatlarını oxuyaraq obyektlər yaradın.**

```python
import json

class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

with open("products.json") as f:
    data = json.load(f)

products = [Product(p["name"], p["price"]) for p in data]
```

**C: JSON faylından işçi məlumatlarını oxuyaraq obyektlər yaradın.**

```python
import json

class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

with open("employees.json") as f:
    data = json.load(f)

employees = [Employee(e["name"], e["salary"]) for e in data]
```

### Sual 72

**A: Fayldakı tələbələri GPA göstəricisinə görə filtrləyin.**

```python
students = [{"name": "Ali", "gpa": 3.5}, {"name": "Vali", "gpa": 2.8}]
filtered = [s for s in students if s["gpa"] >= 3.0]
print(filtered)
```

**B: Fayldakı məhsulları qiymətə görə filtrləyin.**

```python
products = [{"name": "Phone", "price": 500}, {"name": "Pen", "price": 1}]
filtered = [p for p in products if p["price"] >= 100]
print(filtered)
```

**C: Fayldakı işçiləri maaşa görə filtrləyin.**

```python
employees = [{"name": "Ali", "salary": 1000}, {"name": "Vali", "salary": 500}]
filtered = [e for e in employees if e["salary"] >= 800]
print(filtered)
```

### Sual 73

**A: *args, **kwargs və OOP istifadə edərək tələbə sistemi yaradın.**

```python
class Student:
    def __init__(self, name, *grades, **info):
        self.name = name
        self.grades = grades
        self.info = info
    def average(self):
        return sum(self.grades) / len(self.grades)
```

**B: *args, **kwargs və OOP istifadə edərək məhsul sistemi yaradın.**

```python
class Product:
    def __init__(self, name, *prices, **info):
        self.name = name
        self.prices = prices
        self.info = info
    def average_price(self):
        return sum(self.prices) / len(self.prices)
```

**C: *args, **kwargs və OOP istifadə edərək işçi sistemi yaradın.**

```python
class Employee:
    def __init__(self, name, *bonuses, **info):
        self.name = name
        self.bonuses = bonuses
        self.info = info
    def total_bonus(self):
        return sum(self.bonuses)
```

### Sual 74

**A: Birdən çox səviyyəli inheritance istifadə edərək təhsil sistemi yaradın. (Person → Teacher → HeadTeacher)**

```python
class Person:
    def __init__(self, name):
        self.name = name

class Teacher(Person):
    def __init__(self, name, subject):
        super().__init__(name)
        self.subject = subject

class HeadTeacher(Teacher):
    def __init__(self, name, subject, department):
        super().__init__(name, subject)
        self.department = department
```

**B: Birdən çox səviyyəli inheritance istifadə edərək şirkət sistemi yaradın. (Employee → Manager → Director)**

```python
class Employee:
    def __init__(self, name):
        self.name = name

class Manager(Employee):
    def __init__(self, name, team):
        super().__init__(name)
        self.team = team

class Director(Manager):
    def __init__(self, name, team, division):
        super().__init__(name, team)
        self.division = division
```

**C: Birdən çox səviyyəli inheritance istifadə edərək nəqliyyat sistemi yaradın. (Vehicle → Car → ElectricCar)**

```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

class Car(Vehicle):
    def __init__(self, brand, model):
        super().__init__(brand)
        self.model = model

class ElectricCar(Car):
    def __init__(self, brand, model, battery):
        super().__init__(brand, model)
        self.battery = battery
```

### Sual 75

**A: Mini E-Commerce sistemi yaradın (Product, Customer, Order class-ları).**

```python
class Product:
    def __init__(self, name, price):
        self.name = name
        self.price = price

class Customer:
    def __init__(self, name):
        self.name = name

class Order:
    def __init__(self, customer):
        self.customer = customer
        self.products = []
    def add_product(self, product):
        self.products.append(product)
    def total(self):
        return sum(p.price for p in self.products)
```

**B: Mini Kitab Satış Sistemi yaradın (Book, Reader, Order class-ları).**

```python
class Book:
    def __init__(self, title, price):
        self.title = title
        self.price = price

class Reader:
    def __init__(self, name):
        self.name = name

class Order:
    def __init__(self, reader):
        self.reader = reader
        self.books = []
    def add_book(self, book):
        self.books.append(book)
    def total(self):
        return sum(b.price for b in self.books)
```

**C: Mini Restoran Sifariş Sistemi yaradın (Menu, Customer, Order class-ları).**

```python
class Menu:
    def __init__(self, item, price):
        self.item = item
        self.price = price

class Customer:
    def __init__(self, name):
        self.name = name

class Order:
    def __init__(self, customer):
        self.customer = customer
        self.items = []
    def add_item(self, menu_item):
        self.items.append(menu_item)
    def total(self):
        return sum(i.price for i in self.items)
```
