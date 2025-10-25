# 🧠 OOP কী?

**OOP মানে হলো Object-Oriented Programming** —
অর্থাৎ, প্রোগ্রাম লেখার এমন একটি পদ্ধতি যেখানে **সবকিছু Object (বস্তু)** হিসেবে ভাবা হয়।

এই Object-এর মধ্যে থাকে —

- **Data (তথ্য)** ➜ যাকে বলে _Attributes_
- **Behavior (আচরণ/কাজ)** ➜ যাকে বলে _Methods_

---

## 🧩 উদাহরণ দিয়ে বোঝা যাক

ধরো, তুমি একটি “Student” প্রোগ্রাম বানাতে চাও।
তাহলে একজন ছাত্র হলো একটি **Object**, যার কিছু বৈশিষ্ট্য ও কাজ আছে।

### উদাহরণ:

| বিষয়              | উদাহরণ              |
| ----------------- | ------------------- |
| Attributes (তথ্য) | নাম, বয়স, রোল নম্বর |
| Methods (কাজ)     | পড়া(), ফলাফল_দেখা() |

Python-এ এটা এইভাবে করা যায় 👇

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def study(self):
        print(f"{self.name} পড়াশোনা করছে!")

# Object তৈরি
s1 = Student("Rahim", 20)
s1.study()
```

🟢 **Output:**

```
Rahim পড়াশোনা করছে!
```

---

## 🔹 OOP-এর মূল ধারণা

| ধারণা                            | ব্যাখ্যা                               |
| -------------------------------- | -------------------------------------- |
| **1. Class**                     | Object তৈরির নকশা (Blueprint)          |
| **2. Object**                    | Class থেকে তৈরি বাস্তব বস্তু           |
| **3. Inheritance (উত্তরাধিকার)** | এক Class থেকে অন্য Class বৈশিষ্ট্য নেয় |
| **4. Encapsulation (আবদ্ধতা)**   | ডেটা ও ফাংশন একসাথে রাখা               |
| **5. Polymorphism (বহুরূপতা)**   | একই কাজ, কিন্তু ভিন্নভাবে করা যায়      |
| **6. Abstraction (অবস্থান)**     | জটিলতা লুকিয়ে সহজ ইন্টারফেস দেওয়া      |

---

## 🧱 Class এবং Object সহজভাবে

### Class:

> Blueprint বা Design (যেমন “Car” নামের নকশা)

### Object:

> সেই নকশা থেকে তৈরি বাস্তব বস্তু (যেমন “BMW”, “Toyota”)

---

## 🚗 উদাহরণ:

```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

    def start(self):
        print(f"{self.brand} গাড়ি চালু হয়েছে!")

# Object তৈরি
car1 = Car("Toyota", "লাল")
car2 = Car("BMW", "কালো")

car1.start()
car2.start()
```

🟢 **Output:**

```
Toyota গাড়ি চালু হয়েছে!
BMW গাড়ি চালু হয়েছে!
```

---

## 🔑 সংক্ষেপে সারাংশ

| বিষয়           | মানে                                      |
| -------------- | ----------------------------------------- |
| **OOP**        | Object ভিত্তিক প্রোগ্রামিং                |
| **Class**      | Object তৈরির ছাঁচ                         |
| **Object**     | Class থেকে তৈরি জিনিস                     |
| **Attributes** | Object-এর ডেটা                            |
| **Methods**    | Object-এর কাজ                             |
| **Benefits**   | কোড পুনঃব্যবহার, নিরাপত্তা, সংগঠিত কাঠামো |

# 🧠 Class কী?

**Class হলো Object তৈরির নকশা (Blueprint)।**

ভাবো, তুমি যদি অনেকগুলো “Student” বা “Car” তৈরি করতে চাও, তাহলে আগে একটি **Class** বানাবে — যেখানে বলবে প্রতিটি ছাত্র বা গাড়ির কী কী বৈশিষ্ট্য (Attribute) ও কাজ (Method) থাকবে।

> 👉 Class শুধু Design, কিন্তু কোনো বাস্তব জিনিস না।

---

### 🔹 উদাহরণ (ভাবনা):

**Class:** “Student”

- বৈশিষ্ট্য (Attributes): নাম, বয়স, রোল
- কাজ (Methods): পড়া(), পরীক্ষায়_দেওয়া()

এখন এই Class থেকে তুমি যত খুশি Student (Object) তৈরি করতে পারো।

---

### 🔹 Python-এ Class বানানো:

```python
class Student:
    def __init__(self, name, roll):
        self.name = name
        self.roll = roll

    def show_info(self):
        print(f"নাম: {self.name}, রোল: {self.roll}")
```

---

# 🧩 Object কী?

**Object হলো Class-এর একটি বাস্তব রূপ (Instance)।**
Class হলো ছাঁচ (mold), আর Object হলো সেই ছাঁচ থেকে তৈরি জিনিস।

> 🎯 এক কথায়:
> Class = নকশা
> Object = তৈরি জিনিস

---

### 🔹 উদাহরণ:

```python
# Object তৈরি
s1 = Student("Rahim", 1)
s2 = Student("Karim", 2)

# Method কল করা
s1.show_info()
s2.show_info()
```

🟢 **Output:**

```
নাম: Rahim, রোল: 1
নাম: Karim, রোল: 2
```

---

## ⚙️ Class এবং Object-এর সম্পর্ক

| বিষয়             | ব্যাখ্যা                                    |
| ---------------- | ------------------------------------------- |
| **Class**        | Object তৈরির নকশা                           |
| **Object**       | Class থেকে তৈরি বাস্তব জিনিস                |
| **Attribute**    | Object-এর তথ্য                              |
| **Method**       | Object-এর কাজ                               |
| **`__init__()`** | Constructor – Object তৈরি হওয়ার সময় চালু হয় |
| **`self`**       | Object-এর নিজের রেফারেন্স (নিজেকে বোঝায়)    |

---

## 🧠 Constructor (`__init__`)

`__init__()` একটি বিশেষ ফাংশন, যা Object তৈরি হওয়ার সময় স্বয়ংক্রিয়ভাবে চলে।

### উদাহরণ:

```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

car1 = Car("Toyota", "লাল")
print(car1.brand)
print(car1.color)
```

🟢 **Output:**

```
Toyota
লাল
```

---

## 🎯 কেন Class ও Object ব্যবহার করবো?

| সুবিধা                                      | ব্যাখ্যা                                |
| ------------------------------------------- | --------------------------------------- |
| **কোড পুনঃব্যবহারযোগ্য (Reusable)**         | একই Class দিয়ে অনেক Object তৈরি করা যায় |
| **পরিষ্কার কাঠামো (Organized)**             | বড় প্রোগ্রামকে ছোট ছোট অংশে ভাগ করা যায় |
| **সহজ রক্ষণাবেক্ষণ (Maintainable)**         | পরিবর্তন করা সহজ হয়                     |
| **বাস্তব জগতের মডেল (Real-world modeling)** | বাস্তব জিনিসের মতো করে কোড লেখা যায়     |

---

## 📘 সংক্ষেপে সারাংশ

| বিষয়            | মানে                          |
| --------------- | ----------------------------- |
| **Class**       | Object তৈরির নকশা             |
| **Object**      | Class থেকে তৈরি বাস্তব বস্তু  |
| **Attributes**  | Object-এর বৈশিষ্ট্য           |
| **Methods**     | Object-এর কাজ                 |
| **Constructor** | Object তৈরি হওয়ার সময় চালু হয় |
| **self**        | Object-এর নিজস্ব পরিচয়        |

চমৎকার ❤️ তুমি এখন OOP-এর সবচেয়ে গুরুত্বপূর্ণ অংশে এসেছো —
👉 **Inheritance (উত্তরাধিকার)**

চলো একদম সহজভাবে বুঝে ফেলি **Inheritance কী, কেন দরকার, এবং কীভাবে ব্যবহার হয়।**

---

# 🧠 Inheritance কী?

**Inheritance** মানে হলো —
একটা **Class** অন্য একটা **Class-এর বৈশিষ্ট্য ও কাজ (Attributes & Methods)** নিজের মধ্যে **উত্তরাধিকারসূত্রে পায়**।

> সহজ ভাষায়:
> একটা নতুন Class তৈরি করার সময় পুরনো Class-এর কোড আবার লিখতে না হয়ে
> সেটার কোড **পুনঃব্যবহার** করা যায়।

---

## 🎯 কেন Inheritance দরকার?

- কোড বারবার না লিখে **পুনঃব্যবহার (reusability)** করা যায়
- বড় প্রজেক্টে **code সংগঠিত (organized)** রাখা যায়
- নতুন Class সহজে **পুরনো Class-এর ওপর ভিত্তি করে** বানানো যায়

---

## 🧱 ধরো একটি উদাহরণ:

তুমি একটি “Person” Class তৈরি করলে —
তার মধ্যে আছে নাম ও বয়স।

এখন “Student” এবং “Teacher” দুইজনই মানুষ,
তাই তারা “Person” Class থেকে বৈশিষ্ট্য নিতে পারে।

---

### 🔹 Base Class (Parent Class)

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def show_info(self):
        print(f"নাম: {self.name}, বয়স: {self.age}")
```

---

### 🔹 Derived Class (Child Class)

```python
class Student(Person):
    def __init__(self, name, age, roll):
        super().__init__(name, age)   # Parent Class থেকে নেয়া
        self.roll = roll

    def study(self):
        print(f"{self.name} পড়াশোনা করছে।")
```

---

### 🔹 Object তৈরি

```python
s1 = Student("Rahim", 20, 101)
s1.show_info()   # Parent Class-এর মেথড
s1.study()       # নিজের মেথড
```

🟢 **Output:**

```
নাম: Rahim, বয়স: 20
Rahim পড়াশোনা করছে।
```

---

## ⚙️ কী ঘটছে এখানে?

| অংশ                     | মানে                                         |
| ----------------------- | -------------------------------------------- |
| `Person`                | Parent Class                                 |
| `Student(Person)`       | Student Class Person থেকে উত্তরাধিকার পেয়েছে |
| `super().__init__(...)` | Parent Class-এর constructor কল করা হয়েছে     |
| `show_info()`           | Parent Class-এর method                       |
| `study()`               | Child Class-এর নিজস্ব method                 |

---

## 🔁 Inheritance-এর ধরন

| ধরন                        | ব্যাখ্যা                              |
| -------------------------- | ------------------------------------- |
| **Single Inheritance**     | এক Class আরেকটা Class থেকে নেয়        |
| **Multilevel Inheritance** | একটার পর একটা Class উত্তরাধিকার পায়   |
| **Multiple Inheritance**   | এক Class একাধিক Parent Class থেকে নেয় |

---

## 🧩 ১️⃣ Single Inheritance (একস্তরীয় উত্তরাধিকার)

> এক Class আরেকটা Class থেকে বৈশিষ্ট্য নেয়।

অর্থাৎ, একটাই Parent (Base) Class আছে,
এবং একটাই Child (Derived) Class সেটার সব ফিচার ব্যবহার করছে।

---

### 🔹 উদাহরণ:

```python
# Parent Class
class Animal:
    def eat(self):
        print("প্রাণী খাবার খায়।")

# Child Class
class Dog(Animal):
    def bark(self):
        print("কুকুর ঘেউ ঘেউ করে।")

# Object তৈরি
dog1 = Dog()
dog1.eat()   # Parent Class থেকে পাওয়া
dog1.bark()  # নিজের method
```

🟢 **Output:**

```
প্রাণী খাবার খায়।
কুকুর ঘেউ ঘেউ করে।
```

👉 এখানে `Dog` Class, `Animal` Class থেকে বৈশিষ্ট্য নিয়েছে।
এটাই **Single Inheritance**।

---

## 🧱 ২️⃣ Multilevel Inheritance (বহুস্তরীয় উত্তরাধিকার)

> এক Class আরেকটা থেকে নেয়, আর সেটি আবার অন্য Class-কে দেয়।
> মানে একটার পর একটা স্তর।

---

### 🔹 উদাহরণ:

```python
# প্রথম স্তর (Base Class)
class Animal:
    def eat(self):
        print("প্রাণী খাবার খায়।")

# দ্বিতীয় স্তর (Intermediate Class)
class Dog(Animal):
    def bark(self):
        print("কুকুর ঘেউ ঘেউ করে।")

# তৃতীয় স্তর (Derived Class)
class Puppy(Dog):
    def weep(self):
        print("ছোট কুকুর কাঁদে।")

# Object তৈরি
puppy1 = Puppy()
puppy1.eat()   # Animal Class থেকে পাওয়া
puppy1.bark()  # Dog Class থেকে পাওয়া
puppy1.weep()  # নিজের method
```

🟢 **Output:**

```
প্রাণী খাবার খায়।
কুকুর ঘেউ ঘেউ করে।
ছোট কুকুর কাঁদে।
```

👉 এখানে সম্পর্কটা এভাবে:
`Animal → Dog → Puppy`
মানে, **Animal** → Parent, **Dog** → তার Child,
আর **Puppy** হলো Grandchild (Dog-এর সন্তান)।

---

## ⚙️ পার্থক্য এক নজরে

| বিষয়                | Single Inheritance | Multilevel Inheritance   |
| ------------------- | ------------------ | ------------------------ |
| Parent Class সংখ্যা | ১টি                | ১টি, কিন্তু একাধিক স্তরে |
| Child Class সংখ্যা  | ১টি                | একাধিক স্তর থাকতে পারে   |
| উদাহরণ              | `Dog → Animal`     | `Puppy → Dog → Animal`   |
| ব্যবহারের ক্ষেত্র   | সাধারণ ক্ষেত্রে    | জটিল সম্পর্ক বোঝাতে      |

## 🧠 Multiple Inheritance কী?

> **Multiple Inheritance** মানে হলো —
> একটি Class একসাথে একাধিক Class থেকে **উত্তরাধিকার (inherit)** পায়।

অর্থাৎ,

> Child Class → একাধিক Parent Class-এর ফিচার ব্যবহার করতে পারে।

---

## 🎯 সাধারণ উদাহরণ

ধরো, তুমি দুটি Class তৈরি করেছো —
একটা হলো **Teacher**, আরেকটা হলো **Researcher**।
এখন তুমি চাও এমন একটি Class, যা **দুইয়ের কাজই করতে পারবে** —
সেটা হবে **Professor**।

---

### 🔹 উদাহরণ কোড

```python
# Parent Class 1
class Teacher:
    def teach(self):
        print("আমি ক্লাস নিচ্ছি।")

# Parent Class 2
class Researcher:
    def research(self):
        print("আমি গবেষণা করছি।")

# Child Class (Multiple Inheritance)
class Professor(Teacher, Researcher):
    def guide(self):
        print("আমি ছাত্রদের গাইড করছি।")

# Object তৈরি
p1 = Professor()

# Methods কল করা
p1.teach()       # Teacher Class থেকে
p1.research()    # Researcher Class থেকে
p1.guide()       # Professor Class থেকে
```

🟢 **Output:**

```
আমি ক্লাস নিচ্ছি।
আমি গবেষণা করছি।
আমি ছাত্রদের গাইড করছি।
```

---

## ⚙️ কী ঘটছে এখানে?

| অংশ                              | মানে                                             |
| -------------------------------- | ------------------------------------------------ |
| `Teacher`                        | প্রথম Parent Class                               |
| `Researcher`                     | দ্বিতীয় Parent Class                             |
| `Professor(Teacher, Researcher)` | Professor দুই Parent Class থেকে বৈশিষ্ট্য নিচ্ছে |
| `p1.teach()`                     | Teacher থেকে নেয়া method                         |
| `p1.research()`                  | Researcher থেকে নেয়া method                      |
| `p1.guide()`                     | Professor-এর নিজের method                        |

---

## 🔄 যদি দুই Parent-এর একই নামের method থাকে?

Python তখন **MRO (Method Resolution Order)** অনুসরণ করে —
মানে, **যে Class আগে লেখা আছে, তার method আগে চলবে।**

### 🔹 উদাহরণ:

```python
class A:
    def show(self):
        print("Class A থেকে")

class B:
    def show(self):
        print("Class B থেকে")

class C(A, B):  # A আগে আছে
    pass

obj = C()
obj.show()
```

🟢 **Output:**

```
Class A থেকে
```

👉 কারণ `A` আগে লেখা হয়েছে `C(A, B)` তে।
যদি লিখতে `C(B, A)`, তাহলে “Class B থেকে” দেখাতো।

---

## 🧱 বাস্তব উদাহরণ

```python
class Engine:
    def start(self):
        print("ইঞ্জিন চালু হলো।")

class MusicSystem:
    def play_music(self):
        print("সঙ্গীত বাজছে...")

class Car(Engine, MusicSystem):
    def drive(self):
        print("গাড়ি চলছে...")

# Object তৈরি
my_car = Car()
my_car.start()
my_car.play_music()
my_car.drive()
```

🟢 **Output:**

```
ইঞ্জিন চালু হলো।
সঙ্গীত বাজছে...
গাড়ি চলছে...
```

---

## 📘 সারাংশ

| বিষয়                              | মানে                                                                                |
| --------------------------------- | ----------------------------------------------------------------------------------- |
| **Multiple Inheritance**          | এক Child Class একাধিক Parent Class থেকে নেয়                                         |
| **উপকারিতা**                      | একাধিক বৈশিষ্ট্য একত্রে ব্যবহার করা যায়                                             |
| **MRO (Method Resolution Order)** | কোন Parent-এর method আগে চলবে তা নির্ধারণ করে                                       |
| **`super()`**                     | Parent Class-এর method কল করার জন্য ব্যবহার হয় (single বা complex case-এ কাজে লাগে) |

| টার্ম                      | মানে                           |
| -------------------------- | ------------------------------ |
| **Parent/Base Class**      | যেখান থেকে বৈশিষ্ট্য নেওয়া হয়  |
| **Child/Derived Class**    | যে Class বৈশিষ্ট্য নেয়         |
| **Single Inheritance**     | এক Parent → এক Child           |
| **Multilevel Inheritance** | এক Parent → Child → Grandchild |

| বিষয়                    | মানে                                               |
| ----------------------- | -------------------------------------------------- |
| **Inheritance**         | একটি Class অন্য Class থেকে বৈশিষ্ট্য নেয়           |
| **Parent/Base Class**   | যেখান থেকে নেয়া হয়                                 |
| **Child/Derived Class** | যে নেয়                                             |
| **super()**             | Parent Class-এর constructor বা method কল করার জন্য |
| **উপকারিতা**            | কোড পুনঃব্যবহার, সংগঠিত কাঠামো                     |



# 🔹 পলিমরফিজম (Polymorphism) কী?

**Polymorphism** শব্দটির অর্থ হলো — _“বহু রূপ”_।
অর্থাৎ, একই জিনিসের একাধিক রূপ বা কাজ করার একাধিক উপায়।

👉 সহজভাবে বললে, পলিমরফিজম মানে হলো **একই ফাংশন বা মেথড বিভিন্ন অবজেক্টের জন্য ভিন্নভাবে কাজ করতে পারে**।

উদাহরণস্বরূপ, “+” অপারেটর সংখ্যা যোগ করার জন্য ব্যবহার করা যায়, আবার স্ট্রিং জোড়া লাগানোর (concatenate) কাজেও ব্যবহার করা যায়।
এটাই পলিমরফিজম।

```python
# উদাহরণ ১
print(10 + 5)       # সংখ্যা যোগ করে → 15
print("Hello " + "World")  # স্ট্রিং যুক্ত করে → Hello World
```

এখানে `+` একই অপারেটর হলেও, সংখ্যা আর স্ট্রিংয়ের ক্ষেত্রে আলাদা কাজ করছে।

---

#### 🔹 ক্লাস ও অবজেক্টে পলিমরফিজম

পলিমরফিজম OOP (Object-Oriented Programming)-এর একটি গুরুত্বপূর্ণ বৈশিষ্ট্য।
এতে বিভিন্ন ক্লাসে একই নামের মেথড থাকে, কিন্তু প্রতিটি ক্লাসে মেথডের কাজ আলাদা হয়।

```python
class Bird:
    def intro(self):
        print("আমি এক ধরনের পাখি।")
    def flight(self):
        print("আমি উড়তে পারি।")

class Penguin(Bird):
    def flight(self):
        print("আমি উড়তে পারি না, আমি সাঁতার কাটি।")

obj_bird = Bird()
obj_penguin = Penguin()

obj_bird.intro()
obj_bird.flight()

obj_penguin.intro()
obj_penguin.flight()
```

🧩 **আউটপুট:**

```
আমি এক ধরনের পাখি।
আমি উড়তে পারি।
আমি এক ধরনের পাখি।
আমি উড়তে পারি না, আমি সাঁতার কাটি।
```

👉 এখানে দেখা যাচ্ছে, `flight()` মেথড দুই ক্লাসেই আছে, কিন্তু প্রতিটি ক্লাসে এর কাজ আলাদা।
এটাই **method overriding**-এর মাধ্যমে পলিমরফিজম।

---

#### 🔹 ফাংশনে পলিমরফিজম

একই ফাংশন বিভিন্ন অবজেক্টের সাথে কাজ করতে পারে — এটাই ফাংশন-লেভেল পলিমরফিজম।

```python
class Cat:
    def sound(self):
        return "Meow"

class Dog:
    def sound(self):
        return "Woof"

def make_sound(animal):
    print(animal.sound())

cat1 = Cat()
dog1 = Dog()

make_sound(cat1)   # Output: Meow
make_sound(dog1)   # Output: Woof
```

👉 এখানে `make_sound()` ফাংশনটি একইভাবে কাজ করছে, কিন্তু অবজেক্ট ভেদে আউটপুট ভিন্ন হচ্ছে।
এটাই পলিমরফিজম।

---

#### 🔹 পলিমরফিজমের ধরন

| ধরন                           | ব্যাখ্যা                                                                          |
| ----------------------------- | --------------------------------------------------------------------------------- |
| **Compile-time Polymorphism** | পাইথনে এটি নেই, যেমন method overloading (একই নামের একাধিক মেথড) জাভা/সি++ এ থাকে। |
| **Runtime Polymorphism**      | পাইথনে এটি সমর্থন করে — অর্থাৎ মেথড ওভাররাইডিং ও ইনহেরিটেন্স ব্যবহার করে।         |

---

#### 🔹 সারাংশ

| বিষয়           | ব্যাখ্যা                                      |
| -------------- | --------------------------------------------- |
| পলিমরফিজম মানে | একই নামের মেথড বা অপারেটর বিভিন্নভাবে কাজ করা |
| কিভাবে কাজ করে | Method Overriding ও Inheritance এর মাধ্যমে    |
| উদাহরণ         | Operator Overloading (`+`), Method Overriding |

---

#### 🔹 ছোট প্র্যাকটিস

```python
class Shape:
    def area(self):
        pass

class Circle(Shape):
    def area(self):
        print("বৃত্তের ক্ষেত্রফল = πr²")

class Square(Shape):
    def area(self):
        print("বর্গক্ষেত্রের ক্ষেত্রফল = a²")

for shape in (Circle(), Square()):
    shape.area()
```

🧩 **আউটপুট:**

```
বৃত্তের ক্ষেত্রফল = πr²
বর্গক্ষেত্রের ক্ষেত্রফল = a²
```


অবশ্যই 😊 চল একদম সহজভাবে **OOP Encapsulation** বুঝে ফেলি — যেন তুমি নিজের মতো করে মনে রাখতে পারো।

---

# 🐍 Encapsulation (এনক্যাপসুলেশন)

---

### 🔹 ১. “Encapsulation” শব্দের মানে কী?

**Encapsulation** মানে হলো
👉 **“কিছু জিনিসকে একসাথে রেখে তাকে বাইরে থেকে সুরক্ষিত রাখা।”**

যেমন:
তুমি যদি একটি *ওষুধের ক্যাপসুল* ভাবো — ভেতরে অনেক উপাদান (data) থাকে,
কিন্তু বাইরের কেউ সরাসরি ওই উপাদানে হাত দিতে পারে না।
শুধু নির্দিষ্টভাবে ব্যবহার করা যায়।

ঠিক তেমনি প্রোগ্রামিং-এ **Encapsulation** মানে হলো
👉 ডেটা (variable) এবং সেই ডেটার সাথে কাজ করা ফাংশন (method) একই ক্লাসে রাখা,
এবং বাইরের কেউ যেন সরাসরি সেই ডেটা পরিবর্তন করতে না পারে।

---

### 🔹 ২. কেন Encapsulation দরকার?

1. **ডেটা সুরক্ষা** — কেউ যেন ভুলবশত ভ্যারিয়েবল পরিবর্তন না করতে পারে।
2. **নিয়ন্ত্রিত অ্যাক্সেস** — আমরা চাইলে getter ও setter দিয়ে ডেটা দেখা বা বদলানো কন্ট্রোল করতে পারি।
3. **কোড সহজ রাখা** — ক্লাসের ভেতরের ডেটা বাইরে থেকে না ঘাটলে কোডের স্থায়িত্ব বাড়ে।

---

### 🔹 ৩. পাইথনে Encapsulation কিভাবে কাজ করে?

আমরা ক্লাসের ভেতরে ভ্যারিয়েবল তিনভাবে রাখতে পারি 👇

| ধরন           | সিনট্যাক্স   | ব্যবহার                              |
| ------------- | ------------ | ------------------------------------ |
| **Public**    | `variable`   | সবাই অ্যাক্সেস করতে পারে             |
| **Protected** | `_variable`  | সাধারণত ক্লাস ও সাবক্লাসে ব্যবহৃত হয় |
| **Private**   | `__variable` | কেবল ক্লাসের ভেতরে অ্যাক্সেস করা যায় |

---

### 🔹 ৪. উদাহরণ: Private ভ্যারিয়েবল দিয়ে ডেটা সুরক্ষা

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # private variable

    def deposit(self, amount):
        self.__balance += amount

    def withdraw(self, amount):
        if amount <= self.__balance:
            self.__balance -= amount
        else:
            print("পর্যাপ্ত টাকা নেই!")

    def get_balance(self):   # getter method
        return self.__balance

# অবজেক্ট তৈরি
account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # ✅ 1500

# বাইরে থেকে অ্যাক্সেস করতে চাইলে
print(account.__balance)  # ❌ Error হবে
```

🔸 এখানে `__balance` বাইরে থেকে দেখা বা পরিবর্তন করা যাবে না।
এটি ক্লাসের ভেতরেই “লুকানো” আছে।

---

### 🔹 ৫. Getter এবং Setter মেথড

Encapsulation-এ ডেটা দেখা বা পরিবর্তন করতে **getter** ও **setter** ব্যবহার করা হয়।

```python
class Person:
    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    # Getter
    def get_age(self):
        return self.__age

    # Setter
    def set_age(self, age):
        if age > 0:
            self.__age = age
        else:
            print("বয়স নেতিবাচক হতে পারে না!")

# ব্যবহার
p1 = Person("Mamun", 25)
print(p1.get_age())  # ✅ 25
p1.set_age(30)       # বয়স পরিবর্তন হলো
print(p1.get_age())  # ✅ 30
p1.set_age(-5)       # ❌ Error বার্তা দেখাবে
```

🧠 এখানে আমরা নিজের তৈরি নিয়ম মেনে ডেটা পরিবর্তন করছি — এটাই **Encapsulation-এর আসল কাজ**।

---





---



### 🔹 Protected কী?

**Protected variable** এমন ভ্যারিয়েবল যেটি **ক্লাস এবং তার সাবক্লাসের (child class)** ভিতর থেকে অ্যাক্সেস করা যায়,
কিন্তু **বাইরে থেকে করা ঠিক নয়** — যদিও পাইথনে পুরোপুরি রোধ করা হয় না।

👉 Protected ভ্যারিয়েবল শুরু হয় **একটি আন্ডারস্কোর `_`** দিয়ে।

উদাহরণ:

```python
self._balance = 1000
```

এটা কেবল “প্রথাগতভাবে” বোঝায় —

> "এই ভ্যারিয়েবলটা বাইরের কেউ সরাসরি ব্যবহার করবে না!"

---

### 🔹 উদাহরণ: Protected ভ্যারিয়েবল ব্যবহার

```python
class Employee:
    def __init__(self, name, salary):
        self._name = name         # protected variable
        self._salary = salary     # protected variable

    def show_info(self):
        print(f"নাম: {self._name}, বেতন: {self._salary}")

# সাবক্লাস
class Manager(Employee):
    def __init__(self, name, salary, department):
        super().__init__(name, salary)
        self.department = department

    def show_manager_info(self):
        print(f"ম্যানেজার: {self._name}, ডিপার্টমেন্ট: {self.department}")

# অবজেক্ট তৈরি
m1 = Manager("Mamun", 50000, "IT")

# সাবক্লাসের ভেতর থেকে _name অ্যাক্সেস করা যাচ্ছে ✅
m1.show_manager_info()

# বাইরে থেকেও technically অ্যাক্সেস করা যায় ⚠️ (কিন্তু করা উচিত নয়)
print(m1._salary)  # Warning: This breaks encapsulation!
```

🧩 **আউটপুট:**

```
ম্যানেজার: Mamun, ডিপার্টমেন্ট: IT
50000
```

---

### 🔹 মনে রাখার বিষয়

| ধরন           | সিনট্যাক্স   | কোথায় অ্যাক্সেসযোগ্য  | উদাহরণ           |
| ------------- | ------------ | --------------------- | ---------------- |
| **Public**    | `variable`   | ক্লাসের ভিতরে ও বাইরে | `self.name`      |
| **Protected** | `_variable`  | ক্লাস ও সাবক্লাসে     | `self._salary`   |
| **Private**   | `__variable` | কেবল ক্লাসের ভিতরে    | `self.__balance` |

---

### 🔹 সংক্ষিপ্তভাবে বুঝে নাও

| স্তর          | কে অ্যাক্সেস করতে পারে | উদ্দেশ্য                           |
| ------------- | ---------------------- | ---------------------------------- |
| **Public**    | সবাই                   | সাধারণ ডেটা                        |
| **Protected** | ক্লাস + সাবক্লাস       | ভেতরের ব্যবহারের জন্য (আংশিক গোপন) |
| **Private**   | শুধুমাত্র ক্লাস        | সম্পূর্ণ গোপন ডেটা                 |

---

### 🔹 বাস্তব উদাহরণ

ধরো, তুমি একটা **Company Management System** বানাচ্ছো।

* **Public:** কর্মচারীর নাম (সবাই দেখতে পারে)
* **Protected:** কর্মচারীর বেতন (কেবল HR ও ম্যানেজার দেখতে পারে)
* **Private:** কোম্পানির ব্যাংক অ্যাকাউন্ট ডিটেইলস (শুধু কোম্পানি সিস্টেম অ্যাক্সেস করতে পারে)

---

### 🔹 Access Modifiers সারাংশ

🔸 `Public` → সবাই দেখতে পায়
🔸 `Protected` → ক্লাস ও সাবক্লাস দেখতে পারে
🔸 `Private` → কেবল ক্লাসের ভেতরে দেখা যায়

---


### 🔹 ৭. সারাংশ (Summary)

| বিষয়                   | ব্যাখ্যা                                                 |
| ---------------------- | -------------------------------------------------------- |
| **Encapsulation মানে** | ডেটা ও মেথড একত্রে রেখে সেগুলো সুরক্ষিত রাখা             |
| **কেন দরকার**          | নিরাপত্তা, নিয়ন্ত্রণ, কোড পরিষ্কার রাখা                  |
| **কীভাবে করা হয়**      | Private ভ্যারিয়েবল (`__name`) ও Getter/Setter মেথড দিয়ে |
| **উদাহরণ**             | ব্যাংক অ্যাকাউন্ট, মোবাইল অ্যাপ, স্কুল সিস্টেম ইত্যাদি   |

---


# 🎯  **Abstraction (অ্যাবস্ট্রাকশন)** 

---

### 🔹 ১. “Abstraction” মানে কী?

**Abstraction** মানে হলো —
👉 “অপ্রয়োজনীয় বিস্তারিত লুকিয়ে শুধু গুরুত্বপূর্ণ জিনিসটা দেখানো।”

বাস্তব উদাহরণ দিই 👇
তুমি যখন মোবাইল ফোনে ছবি তোল,
তুমি শুধু “Camera App” খুলে বোতাম টিপো 📸
কিন্তু ভিতরে কত জটিল কোড, সেন্সর, ডেটা প্রসেসিং — এসব তুমি জানো না।
তুমি শুধু **সহজ ইন্টারফেস** দেখো।

এটাই **Abstraction** —

> ব্যবহারকারীকে কেবল দরকারি অংশ দেখানো,
> বাকি জটিল অংশ লুকিয়ে রাখা।

---

### 🔹 ২. প্রোগ্রামিং-এ Abstraction কেন দরকার?

1. **কোডকে সহজ রাখা** — জটিল অংশ লুকিয়ে দিলে বুঝতে সহজ হয়।
2. **রিইউজেবল কোড** — একই বেস ক্লাস থেকে অনেক ক্লাস বানানো যায়।
3. **সিকিউরিটি** — ব্যবহারকারীকে কেবল প্রয়োজনীয় ফাংশন দেওয়া হয়।

---

### 🔹 ৩. পাইথনে Abstraction কিভাবে করা যায়?

পাইথনে আমরা **`abc` (Abstract Base Class)** নামের একটি মডিউল ব্যবহার করি।

এখানে আমরা এমন কিছু **abstract class** তৈরি করি, যেগুলো থেকে সাবক্লাস ইনহেরিট করে
নিজস্বভাবে মেথডগুলোর কাজ লিখতে পারে।

---

### 🔹 ৪. উদাহরণ: Abstract Class ও Method

```python
from abc import ABC, abstractmethod

# Abstract Class
class Shape(ABC):
    @abstractmethod
    def area(self):
        pass   # শুধু নাম আছে, কাজ নেই

# Subclass 1
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

# Subclass 2
class Rectangle(Shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

# অবজেক্ট তৈরি
c = Circle(5)
r = Rectangle(4, 6)

print("Circle Area:", c.area())
print("Rectangle Area:", r.area())
```

🧩 **আউটপুট:**

```
Circle Area: 78.5
Rectangle Area: 24
```

---

### 🔹 ৫. এখানে কী ঘটল?

1. `Shape` হলো একটি **abstract class**,
   যেখানে `area()` শুধু ঘোষণা করা আছে কিন্তু কাজ লেখা হয়নি।
2. `Circle` ও `Rectangle` হলো **subclass**,
   তারা `area()` মেথড নিজেদের মতো করে **implement** করেছে।
3. আমরা সরাসরি `Shape` ক্লাসের অবজেক্ট বানাতে পারি না।
   কারণ সেটি অসম্পূর্ণ (abstract)।

---

### 🔹 ৬. কেন সরাসরি abstract class ব্যবহার করা যায় না?

```python
s = Shape()  # ❌ Error!
```

🧩 **Error:**

```
TypeError: Can't instantiate abstract class Shape with abstract method area
```

👉 কারণ abstract class শুধু “ধারণা” দেয়, কাজ নয়।
যে ক্লাসটি তা থেকে ইনহেরিট করবে, সেই ক্লাস কাজ লিখে দেবে।

---

### 🔹 ৭. সহজভাবে বোঝো

ধরো, `Shape` ক্লাসটা হলো **“নকশা” (blueprint)** —
তাতে বলা আছে, “আমার একটা `area()` নামের ফাংশন থাকবে।”
কিন্তু **কীভাবে** কাজ করবে, সেটা বলে না।

সেই কাজটা সাবক্লাস (যেমন Circle, Rectangle) নিজের মতো করে নির্ধারণ করে।

---

### 🔹 ৮. সারাংশ

| বিষয়                 | ব্যাখ্যা                                     |
| -------------------- | -------------------------------------------- |
| **Abstraction মানে** | অপ্রয়োজনীয় অংশ লুকিয়ে কেবল দরকারি অংশ দেখানো |
| **কীভাবে করা হয়**    | Abstract Class ও Abstract Method ব্যবহার করে |
| **মডিউল**            | `abc`                                        |
| **উদাহরণ**           | Shape → Circle, Rectangle                    |
| **উদ্দেশ্য**         | কোড সহজ, রিইউজেবল ও পরিষ্কার রাখা            |

---

### 🔹 ৯. বাস্তব উদাহরণ

ধরো তুমি একটা **Payment System** বানাচ্ছো।

```python
from abc import ABC, abstractmethod

class Payment(ABC):
    @abstractmethod
    def pay(self, amount):
        pass

class Bkash(Payment):
    def pay(self, amount):
        print(f"{amount} টাকা বিকাশে পাঠানো হলো।")

class Nagad(Payment):
    def pay(self, amount):
        print(f"{amount} টাকা নগদে পাঠানো হলো।")

# ব্যবহার
p1 = Bkash()
p2 = Nagad()

p1.pay(500)
p2.pay(800)
```

🧩 **আউটপুট:**

```
500 টাকা বিকাশে পাঠানো হলো।
800 টাকা নগদে পাঠানো হলো।
```

👉 এখানে `Payment` হলো abstract class,
আর `Bkash`, `Nagad` ক্লাস হলো তার বাস্তব রূপ (implementation)।

---
