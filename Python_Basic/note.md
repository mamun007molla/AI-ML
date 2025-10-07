# Day-1

## 🧩 Variables (ভেরিয়েবল) কী?

**ভেরিয়েবল** হলো একটি **নাম দেওয়া জায়গা (container)** যেখানে আমরা কোনো ডেটা সংরক্ষণ করি।
যেমন আপনি ক্যালকুলেটরে কোনো সংখ্যা রেখে দেন পরে ব্যবহার করার জন্য — Python-এ ভেরিয়েবলও ঠিক তেমন কাজ করে।

### ✅ উদাহরণ:

```python
name = "Mamun"
age = 25
height = 5.9
```

🔹 এখানে

* `name` ভেরিয়েবলটি **একটা string** (লেখা) রাখছে
* `age` ভেরিয়েবলটি **একটা integer** (পুরো সংখ্যা) রাখছে
* `height` ভেরিয়েবলটি **একটা float** (দশমিক সংখ্যা) রাখছে

---

## 🧠 ভেরিয়েবল সম্পর্কে কিছু নিয়ম:

1. ভেরিয়েবলের নাম শুধু **অক্ষর, সংখ্যা এবং _ (underscore)** দিয়ে তৈরি করা যায়।
2. নামের শুরু **সংখ্যা দিয়ে হবে না।**
3. Python **case-sensitive**, তাই `Name` আর `name` আলাদা।
4. সাধারণভাবে ছোট অক্ষর ব্যবহার করা ভালো, যেমন `student_name`, `total_price` ইত্যাদি।

---

## 🧮 Data Types (ডেটা টাইপ) কী?

Python-এ বিভিন্ন ধরনের ডেটা রাখতে হলে সেগুলোর **ধরন (type)** জানতে হয়।
যেমন সংখ্যা, লেখা, লজিকাল মান ইত্যাদি।

### 🎯 সাধারণ কিছু Data Type নিচে দেওয়া হলো:

| Data Type | উদাহরণ                                  | বর্ণনা                                  |
| --------- | --------------------------------------- | --------------------------------------- |
| **int**   | `age = 20`                              | পূর্ণ সংখ্যা (integer)                  |
| **float** | `pi = 3.14`                             | দশমিক সংখ্যা                            |
| **str**   | `name = "Mamun"`                        | টেক্সট বা string                        |
| **bool**  | `is_happy = True`                       | সত্য/মিথ্যা (True/False)                |
| **list**  | `fruits = ["apple", "banana", "mango"]` | একাধিক মান একসাথে রাখতে ব্যবহৃত         |
| **tuple** | `colors = ("red", "green", "blue")`     | লিস্টের মতো, কিন্তু পরিবর্তন করা যায় না |
| **dict**  | `person = {"name": "Mamun", "age": 25}` | কী-ভ্যালু জোড়ায় ডেটা রাখে               |
| **set**   | `numbers = {1, 2, 3}`                   | ইউনিক মান রাখে (একই মান বারবার থাকে না) |

---

## 🧾 উদাহরণসহ ব্যাখ্যা

```python
# Integer
x = 10

# Float
y = 5.5

# String
name = "Mamun"

# Boolean
is_student = True

# List
numbers = [1, 2, 3, 4, 5]

# Dictionary
student = {"name": "Mamun", "age": 25}

# Tuple
coordinates = (10, 20)

# Set
unique_numbers = {1, 2, 3}
```

---

## 🔍 টাইপ পরীক্ষা করা যায়:

Python-এ `type()` ফাংশন দিয়ে দেখা যায় কোনো ভেরিয়েবল কোন ধরনের।

```python
x = 10
print(type(x))
```

➡️ আউটপুট হবে: `<class 'int'>`

---

## 🪄 সংক্ষেপে মনে রাখার টিপস:

* ভেরিয়েবল হলো ডেটা রাখার **বাক্স**।
* ডেটা টাইপ বলে দেয় **কেমন ধরনের** ডেটা আছে।
* Python স্বয়ংক্রিয়ভাবে টাইপ নির্ধারণ করে (তাই টাইপ লিখতে হয় না)।


## 🧠 ইনপুট (Input) কী?

**Input** মানে ব্যবহারকারীর কাছ থেকে তথ্য নেওয়া।
যেমন — আপনি কোনো প্রোগ্রাম চালালে, সেটা যদি আপনার নাম বা বয়স জানতে চায় — সেটাই ইনপুট নেওয়া।

Python-এ ইনপুট নেওয়ার জন্য ব্যবহার করা হয় 👉 **`input()`** ফাংশন।

---

## 🧩 বেসিক ইনপুট উদাহরণ

```python
name = input("তোমার নাম লিখো: ")
print("হ্যালো,", name)
```

### 🧾 ব্যাখ্যা:

* `input()` ব্যবহার করলে প্রোগ্রাম থেমে যায় এবং ব্যবহারকারীর কাছ থেকে কিছু টাইপ করার অপেক্ষা করে।
* আপনি যা টাইপ করবেন, তা **string** হিসেবে `name` ভেরিয়েবলে জমা হবে।
* তারপর `print()` দিয়ে সেটি দেখানো হয়।

🖥️ যদি আপনি লেখেন:

```
তোমার নাম লিখো: Mamun
```

আউটপুট হবে:

```
হ্যালো, Mamun
```

---

## 🧮 সংখ্যা (Number) ইনপুট নেওয়া

`input()` সব সময় **string** রিটার্ন করে।
তাই সংখ্যা হিসেবে ব্যবহার করতে চাইলে সেটি **রূপান্তর (convert)** করতে হয়।

```python
age = input("তোমার বয়স লিখো: ")
print(age + 5)  # ❌ Error হবে, কারণ age string
```

এই ভুল ঠিক করতে হবে এভাবে 👇

### ✅ সঠিক পদ্ধতি:

```python
age = int(input("তোমার বয়স লিখো: "))
print("৫ বছর পর তোমার বয়স হবে:", age + 5)
```

🔹 এখানে `int()` ইনপুটটাকে integer (সংখ্যা) এ রূপান্তর করেছে।

---

## 🔢 দশমিক সংখ্যা (Float) ইনপুট

যদি দশমিক সংখ্যা নিতে চান, ব্যবহার করুন `float()`।

```python
height = float(input("তোমার উচ্চতা (মিটার): "))
print("তোমার উচ্চতা:", height, "মিটার")
```

---

## 🧰 একাধিক ইনপুট একসাথে নেওয়া

আপনি চাইলে এক লাইনেই একাধিক ইনপুট নিতে পারেন।

```python
name, age = input("নাম ও বয়স লিখো (space দিয়ে): ").split()
print("নাম:", name)
print("বয়স:", age)
```

🖥️ উদাহরণ ইনপুট:

```
Mamun 25
```

➡️ আউটপুট:

```
নাম: Mamun
বয়স: 25
```

---

## 🧾 প্র্যাকটিস এক্সারসাইজ 🎯

1️⃣ ব্যবহারকারীর কাছ থেকে নাম ও বয়স ইনপুট নিয়ে নিচের আউটপুট দেখাও:

```
হ্যালো Mamun! তোমার বয়স ২৫ বছর।
```

2️⃣ দুটি সংখ্যা ইনপুট নিয়ে তাদের যোগফল প্রিন্ট করো।

3️⃣ কোনো ছাত্রের নাম, ক্লাস, এবং GPA ইনপুট নিয়ে সুন্দরভাবে প্রিন্ট করো।



## ⚙️ অপারেটর (Operator) কী?

**Operator** হলো একটি **চিহ্ন (symbol)** বা **চিহ্নের সমষ্টি**, যা কোনো **মান (value)** বা **ভেরিয়েবলের উপর কাজ (operation)** করে।
যেমন – যোগ (+), বিয়োগ (-), গুণ (*), ভাগ (/) ইত্যাদি।

---

## 🧩 অপারেটরের ধরন (Types of Operators)

Python-এ মূলত ৭ ধরনের অপারেটর আছে 👇

| ধরন | নাম                  | কাজ                                     |
| --- | -------------------- | --------------------------------------- |
| 1️⃣ | Arithmetic Operators | গাণিতিক কাজ করে                         |
| 2️⃣ | Assignment Operators | মান (value) অ্যাসাইন করে                |
| 3️⃣ | Comparison Operators | তুলনা করে (বড়, ছোট, সমান ইত্যাদি)       |
| 4️⃣ | Logical Operators    | লজিক্যাল (and, or, not) কাজ করে         |
| 5️⃣ | Identity Operators   | অবজেক্ট একই কি না পরীক্ষা করে           |
| 6️⃣ | Membership Operators | কোনো মান লিস্ট/স্ট্রিং-এ আছে কি না দেখে |
| 7️⃣ | Bitwise Operators    | বাইনারি বিটের উপর কাজ করে               |

---

## 🔢 1️⃣ Arithmetic Operators (গাণিতিক অপারেটর)

| Operator | উদাহরণ   | ফলাফল              |
| -------- | -------- | ------------------ |
| `+`      | `a + b`  | যোগ                |
| `-`      | `a - b`  | বিয়োগ              |
| `*`      | `a * b`  | গুণ                |
| `/`      | `a / b`  | ভাগ (দশমিক সহ)     |
| `//`     | `a // b` | পূর্ণসংখ্যা ভাগফল  |
| `%`      | `a % b`  | ভাগশেষ (remainder) |
| `**`     | `a ** b` | ঘাত (power)        |

🔹 উদাহরণ:

```python
a = 10
b = 3
print(a + b)   # 13
print(a // b)  # 3
print(a ** b)  # 1000
```

---

## 🧭 2️⃣ Assignment Operators (অ্যাসাইনমেন্ট অপারেটর)

| Operator | উদাহরণ   | সমান অর্থ |
| -------- | -------- | --------- |
| `=`      | `x = 5`  | x = 5     |
| `+=`     | `x += 3` | x = x + 3 |
| `-=`     | `x -= 2` | x = x - 2 |
| `*=`     | `x *= 4` | x = x * 4 |
| `/=`     | `x /= 2` | x = x / 2 |

🔹 উদাহরণ:

```python
x = 5
x += 3   # এখন x = 8
print(x)
```

---

## ⚖️ 3️⃣ Comparison Operators (তুলনা অপারেটর)

| Operator | অর্থ          | উদাহরণ   |
| -------- | ------------- | -------- |
| `==`     | সমান কি না    | `a == b` |
| `!=`     | সমান নয় কি না | `a != b` |
| `>`      | বড় কি না      | `a > b`  |
| `<`      | ছোট কি না     | `a < b`  |
| `>=`     | বড় বা সমান    | `a >= b` |
| `<=`     | ছোট বা সমান   | `a <= b` |

🔹 উদাহরণ:

```python
a = 10
b = 5
print(a > b)   # True
print(a == b)  # False
```

---

## 🧠 4️⃣ Logical Operators (লজিক্যাল অপারেটর)

| Operator | কাজ                    | উদাহরণ             |
| -------- | ---------------------- | ------------------ |
| `and`    | দুই শর্তই সত্য হতে হবে | `a > 5 and b < 10` |
| `or`     | একটিও সত্য হলে হবে     | `a > 5 or b < 2`   |
| `not`    | ফলাফল উল্টে দেয়        | `not(a > b)`       |

🔹 উদাহরণ:

```python
x = 10
print(x > 5 and x < 15)  # True
print(x > 20 or x == 10) # True
print(not(x == 10))      # False
```

---

## 🪪 5️⃣ Identity Operators (আইডেন্টিটি অপারেটর)

| Operator | কাজ                           | উদাহরণ       |
| -------- | ----------------------------- | ------------ |
| `is`     | একই অবজেক্ট কি না পরীক্ষা করে | `a is b`     |
| `is not` | একই না হলে True               | `a is not b` |

🔹 উদাহরণ:

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]
print(a is b)      # True
print(a is c)      # False
```

---

## 🔍 6️⃣ Membership Operators (মেম্বারশিপ অপারেটর)

| Operator | কাজ                | উদাহরণ               |
| -------- | ------------------ | -------------------- |
| `in`     | কোনো মান আছে কি না | `'a' in 'apple'`     |
| `not in` | কোনো মান নেই কি না | `'x' not in 'apple'` |

🔹 উদাহরণ:

```python
fruits = ["apple", "banana"]
print("apple" in fruits)      # True
print("mango" not in fruits)  # True
```

---

## 💡 7️⃣ Bitwise Operators (বিটওয়াইজ অপারেটর)

এই অপারেটরগুলো **বাইনারি (0/1)** মান নিয়ে কাজ করে।

| Operator | নাম         | কাজ             |                       |
| -------- | ----------- | --------------- | --------------------- |
| `&`      | AND         | উভয় বিট 1 হলে 1 |                       |
| `        | `           | OR              | যেকোনো এক বিট 1 হলে 1 |
| `^`      | XOR         | একটাই 1 হলে 1   |                       |
| `~`      | NOT         | বিট উল্টে দেয়   |                       |
| `<<`     | Left Shift  | বিট বামে সরায়   |                       |
| `>>`     | Right Shift | বিট ডানে সরায়   |                       |

🔹 উদাহরণ:

```python
a = 5   # 0101
b = 3   # 0011
print(a & b)  # 1
print(a | b)  # 7
```

---

## 🎯 প্র্যাকটিস এক্সারসাইজ

1️⃣ দুটি সংখ্যা ইনপুট নিয়ে তাদের উপর সব Arithmetic অপারেশন করে ফলাফল দেখাও।
2️⃣ ব্যবহারকারীর বয়স ইনপুট নিয়ে দেখাও সে প্রাপ্তবয়স্ক কি না (>= 18 হলে প্রাপ্তবয়স্ক)।
3️⃣ লিস্টে কোনো আইটেম আছে কি না `in` অপারেটর দিয়ে যাচাই করো।
4️⃣ `and`, `or`, `not` অপারেটরের উদাহরণ লিখে আউটপুট বের করো।



## ⚙️ Precedence (প্রাধান্য) কী?

**Precedence** মানে হলো,
যখন কোনো এক্সপ্রেশনে একাধিক অপারেটর থাকে, তখন **কোন অপারেটর আগে কাজ করবে** — সেটাই নির্ধারণ করে **Precedence**।

👉 উদাহরণ:

```python
x = 10 + 5 * 2
```

এখানে `+` এবং `*` দুটো অপারেটর আছে।
এখন প্রশ্ন — আগে যোগ না গুণ হবে?

➡️ উত্তর: **গুণ (`*`) এর precedence বেশি**, তাই আগে গুণ হবে।

🔹 ধাপে ধাপে:

```
10 + 5 * 2
= 10 + 10
= 20
```

---

## 🔁 Associativity (দিক বা দিকনির্দেশ) কী?

**Associativity** বলে দেয়,
যদি একই precedence-এর একাধিক অপারেটর থাকে, তাহলে **বাম দিক থেকে কাজ হবে নাকি ডান দিক থেকে।**

👉 উদাহরণ:

```python
x = 10 - 5 + 2
```

এখানে `-` এবং `+` দুইটারই **একই precedence**।
তাই Python **বাম দিক থেকে (Left to Right)** কাজ করে।

🔹 ধাপে ধাপে:

```
10 - 5 + 2
= (10 - 5) + 2
= 5 + 2
= 7
```

---

## 🧩 কিছু সাধারণ অপারেটরের Precedence তালিকা (উচ্চ থেকে নিম্ন ক্রমে)

| ক্রম | অপারেটর                          | কাজ                            | Associativity |
| ---- | -------------------------------- | ------------------------------ | ------------- |
| 1️⃣  | `()`                             | Parentheses                    | Left to Right |
| 2️⃣  | `**`                             | Exponentiation (power)         | Right to Left |
| 3️⃣  | `*`, `/`, `//`, `%`              | Multiplication, Division, etc. | Left to Right |
| 4️⃣  | `+`, `-`                         | Addition, Subtraction          | Left to Right |
| 5️⃣  | `<`, `<=`, `>`, `>=`, `==`, `!=` | Comparison                     | Left to Right |
| 6️⃣  | `not`                            | Logical NOT                    | Right to Left |
| 7️⃣  | `and`                            | Logical AND                    | Left to Right |
| 8️⃣  | `or`                             | Logical OR                     | Left to Right |
| 9️⃣  | `=`                              | Assignment                     | Right to Left |

---

## 🧮 উদাহরণ ব্যাখ্যা

### 🔹 উদাহরণ ১:

```python
x = 5 + 3 * 2
print(x)
```

➡️ Output: `11`
কারণ `*` আগে কাজ করবে: `3*2 = 6`, তারপর `5+6 = 11`

---

### 🔹 উদাহরণ ২:

```python
x = (5 + 3) * 2
print(x)
```

➡️ Output: `16`
কারণ এখানে `()` দিয়ে **precedence override** করা হয়েছে।

---

### 🔹 উদাহরণ ৩:

```python
x = 2 ** 3 ** 2
print(x)
```

➡️ Output: `512`

🔹 ব্যাখ্যা:
`**` এর associativity হলো **Right to Left**
তাই হবে `2 ** (3 ** 2)` → `2 ** 9 = 512`

---

## 🎯 প্র্যাকটিস এক্সারসাইজ

1️⃣ নিচের এক্সপ্রেশনগুলোর আউটপুট বের করো এবং কারণ লিখো:

```python
a = 10 + 2 * 3
b = (10 + 2) * 3
```

2️⃣ নিচের কোডের আউটপুট কী হবে?

```python
x = 5 + 2 ** 3 * 2
```

3️⃣ `**`, `/`, `//`, `%` অপারেটর ব্যবহার করে একটি এক্সপ্রেশন লিখো এবং Precedence অনুযায়ী ব্যাখ্যা করো।

4️⃣ `2 ** 3 ** 2` কেন 512 হয়, সেটা প্রমাণ করে দেখাও।



## 🧠 **Python-এর মৌলিক Data Structure**

Python-এ Data Structure মানে হলো — এমন কিছু পদ্ধতি বা উপায় যার মাধ্যমে আমরা ডেটা **সংরক্ষণ (store)**, **পরিচালনা (manage)** এবং **অ্যাক্সেস (access)** করতে পারি।

Python-এর প্রধান বিল্ট-ইন (Built-in) Data Structure গুলো হলো 👇

---

### 🟩 1. **List (লিস্ট)**

* এটি একটি **ordered** এবং **mutable (পরিবর্তনযোগ্য)** ডেটা স্ট্রাকচার।
* একাধিক আইটেম (যেমন সংখ্যা, স্ট্রিং, অন্য লিস্ট ইত্যাদি) একসাথে সংরক্ষণ করা যায়।

**উদাহরণ:**

```python
numbers = [10, 20, 30, 40]
fruits = ["apple", "banana", "mango"]
print(numbers[2])     # 30
fruits.append("orange")  # নতুন আইটেম যোগ করা
```

✅ বৈশিষ্ট্য:

* index ব্যবহার করে অ্যাক্সেস করা যায়
* append(), remove(), sort() ইত্যাদি অনেক মেথড আছে
* nested list রাখা যায়


## 🧠 List Methods কী?

**List Methods** হলো কিছু বিল্ট-ইন ফাংশন (built-in functions) যেগুলোর সাহায্যে আমরা লিস্টের মধ্যে **মান যোগ, বাদ, পরিবর্তন, সাজানো** ইত্যাদি কাজ করতে পারি।

---

## 🧾 সবচেয়ে ব্যবহৃত List Methods 👇

| মেথড          | কাজ                                                     | উদাহরণ                             |
| ------------- | ------------------------------------------------------- | ---------------------------------- |
| **append()**  | লিস্টের শেষে একটি নতুন মান যোগ করে                      | `fruits.append("orange")`          |
| **insert()**  | নির্দিষ্ট ইনডেক্সে মান যোগ করে                          | `fruits.insert(1, "grape")`        |
| **remove()**  | কোনো নির্দিষ্ট মান মুছে দেয়                             | `fruits.remove("banana")`          |
| **pop()**     | ইনডেক্স অনুযায়ী মান মুছে দেয় (না দিলে শেষেরটা মুছে দেয়) | `fruits.pop()` বা `fruits.pop(1)`  |
| **clear()**   | লিস্ট পুরোপুরি খালি করে                                 | `fruits.clear()`                   |
| **sort()**    | লিস্ট সাজায় (ascending বা descending)                   | `fruits.sort()`                    |
| **reverse()** | লিস্ট উল্টে দেয়                                         | `fruits.reverse()`                 |
| **copy()**    | লিস্টের কপি তৈরি করে                                    | `new_list = fruits.copy()`         |
| **count()**   | কোনো মান কয়বার আছে তা গুনে                              | `fruits.count("apple")`            |
| **index()**   | কোনো মানের ইনডেক্স নম্বর দেয়                            | `fruits.index("banana")`           |
| **extend()**  | এক লিস্টের সাথে অন্য লিস্ট যোগ করে                      | `fruits.extend(["kiwi", "melon"])` |

---

## 🧮 উদাহরণ ১:

```python
fruits = ["apple", "banana", "mango"]
fruits.append("orange")
print(fruits)
```

➡️ Output:

```
['apple', 'banana', 'mango', 'orange']
```

---

## 🧮 উদাহরণ ২:

```python
numbers = [1, 3, 2, 5, 4]
numbers.sort()
print(numbers)
```

➡️ Output:

```
[1, 2, 3, 4, 5]
```

---

## 🧮 উদাহরণ ৩:

```python
nums = [10, 20, 30, 40]
nums.pop(2)
print(nums)
```

➡️ Output:

```
[10, 20, 40]
```

---

## 🧮 উদাহরণ ৪:

```python
a = [1, 2, 3]
b = [4, 5]
a.extend(b)
print(a)
```

➡️ Output:

```
[1, 2, 3, 4, 5]
```

---

## 🧮 উদাহরণ ৫:

```python
letters = ["a", "b", "c"]
letters.reverse()
print(letters)
```

➡️ Output:

```
['c', 'b', 'a']
```

---

## 💡 অতিরিক্ত তথ্য:

* **`append()`** একবারে একটি মান যোগ করে
* **`extend()`** একবারে একাধিক মান যোগ করতে পারে
* **`sort(reverse=True)`** দিলে descending অর্ডারে সাজায়

---

## 🎯 প্র্যাকটিস এক্সারসাইজ

1️⃣ একটি লিস্ট তৈরি করো: `["apple", "banana", "cherry"]`
 → শেষে `"mango"` যোগ করো
 → `"banana"` মুছে দাও

2️⃣ একটি লিস্ট `[5, 2, 9, 1, 7]` সাজিয়ে ascending ও descending অর্ডারে দেখাও।

3️⃣ একটি লিস্টে `"a"` কয়বার আছে তা গুনে বের করো।

4️⃣ দুটি লিস্ট `[1, 2, 3]` এবং `[4, 5, 6]` একত্র করো।

5️⃣ একটি লিস্ট উল্টো করে দেখাও (reverse)।


---

### 🟨 2. **Tuple (টিউপল)**

* এটি **ordered** কিন্তু **immutable (পরিবর্তনযোগ্য নয়)**।
* একবার তৈরি হলে এর মান পরিবর্তন করা যায় না।

**উদাহরণ:**

```python
coordinates = (10, 20)
print(coordinates[0])   # 10
```

✅ বৈশিষ্ট্য:

* নিরাপদ ডেটা স্টোরের জন্য ভালো
* লিস্টের তুলনায় দ্রুত কাজ করে

---

### 🟦 3. **Set (সেট)**

* এটি **unordered** এবং **unique items** রাখে (একই মান একাধিকবার রাখা যায় না)।
* গাণিতিক সেটের মতো কাজ করে (union, intersection ইত্যাদি)।

**উদাহরণ:**

```python
numbers = {1, 2, 3, 3, 4}
print(numbers)       # {1, 2, 3, 4}
numbers.add(5)
numbers.remove(2)
```

✅ বৈশিষ্ট্য:

* ডুপ্লিকেট ভ্যালু থাকে না
* দ্রুত membership test (যেমন: `if x in set:`)

---

### 🟥 4. **Dictionary (ডিকশনারি)**

* এটি **key-value pair** আকারে ডেটা রাখে।
* প্রতিটি key অনন্য (unique) হতে হবে।

**উদাহরণ:**

```python
student = {"name": "Mamun", "age": 22, "dept": "CSE"}
print(student["name"])      # Mamun
student["age"] = 23         # মান পরিবর্তন করা
```

✅ বৈশিষ্ট্য:

* দ্রুত লুকআপ, আপডেট, ও ডিলিশন করা যায়
* JSON ডেটার মতো কাজ করে

---

## 🧩 **সারসংক্ষেপ:**

| Data Structure | Ordered | Mutable | Duplicate | Syntax Example     |
| -------------- | ------- | ------- | --------- | ------------------ |
| List           | ✅       | ✅       | ✅         | `[1, 2, 3]`        |
| Tuple          | ✅       | ❌       | ✅         | `(1, 2, 3)`        |
| Set            | ❌       | ✅       | ❌         | `{1, 2, 3}`        |
| Dictionary     | ❌       | ✅       | ❌ (key)   | `{"a": 1, "b": 2}` |





## 🧠 **Python Extended / Advanced Data Structures (বিস্তারিতভাবে)**

---

### 🟩 1. **Stack (স্ট্যাক)**

**ধারণা:**
Stack হলো একটি **LIFO (Last In First Out)** ডেটা স্ট্রাকচার।
অর্থাৎ, যে আইটেমটি শেষে ঢোকে, সেটিই প্রথমে বের হয়।

**উদাহরণ:**

```python
stack = []
stack.append(10)
stack.append(20)
stack.append(30)
print(stack)     # [10, 20, 30]

stack.pop()      # শেষের আইটেম বের করবে (30)
print(stack)     # [10, 20]
```

✅ **ব্যবহার:**

* Undo/Redo সিস্টেম
* Function Call Stack
* Expression evaluation

---

### 🟨 2. **Queue (কিউ)**

**ধারণা:**
Queue হলো একটি **FIFO (First In First Out)** ডেটা স্ট্রাকচার।
অর্থাৎ, যে আইটেমটি আগে ঢোকে, সেটিই আগে বের হয়।

**উদাহরণ:**

```python
from collections import deque

queue = deque()
queue.append(10)
queue.append(20)
queue.append(30)
print(queue)       # deque([10, 20, 30])

queue.popleft()    # প্রথম আইটেম বের হবে (10)
print(queue)       # deque([20, 30])
```

✅ **ব্যবহার:**

* Task scheduling
* Message processing
* Resource sharing

---

### 🟦 3. **Linked List (লিংকড লিস্ট)**

**ধারণা:**
একটি লিংকড লিস্ট হলো নোডের (node) একটি সিরিজ, যেখানে প্রতিটি নোডে ডেটা ও পরবর্তী নোডের ঠিকানা (pointer) থাকে।

**সাধারণ উদাহরণ (কাস্টম ইমপ্লিমেন্টেশন):**

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def insert(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def display(self):
        current = self.head
        while current:
            print(current.data, end=" -> ")
            current = current.next

ll = LinkedList()
ll.insert(10)
ll.insert(20)
ll.insert(30)
ll.display()   # 30 -> 20 -> 10 ->
```

✅ **ব্যবহার:**

* Dynamic memory allocation
* Insertion/Deletion সহজ

---

### 🟥 4. **Tree (ট্রি)**

**ধারণা:**
Tree হলো একটি hierarchical structure যেখানে data parent-child সম্পর্কের মাধ্যমে সংরক্ষিত হয়।

**উদাহরণ: Binary Tree**

```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

root = Node(10)
root.left = Node(5)
root.right = Node(15)
```

✅ **ব্যবহার:**

* Binary Search Tree
* File directory structure
* Data indexing

---

### 🟪 5. **Graph (গ্রাফ)**

**ধারণা:**
Graph হলো নোড (vertices) এবং তাদের সংযোগ (edges) দ্বারা গঠিত একটি স্ট্রাকচার।

**উদাহরণ:**

```python
graph = {
    "A": ["B", "C"],
    "B": ["A", "D"],
    "C": ["A", "D"],
    "D": ["B", "C"]
}
```

✅ **ব্যবহার:**

* Social network connection
* Shortest path algorithm (Dijkstra, BFS, DFS)
* Web crawler

---

### 🟫 6. **Heap (হিপ)**

**ধারণা:**
Heap একটি বিশেষ Binary Tree যেখানে প্রতিটি parent node তার child node এর তুলনায় ছোট (Min-Heap) বা বড় (Max-Heap) হয়।

**উদাহরণ:**

```python
import heapq

numbers = [5, 1, 8, 3]
heapq.heapify(numbers)
print(numbers)    # [1, 3, 8, 5]  (Min-Heap)
heapq.heappush(numbers, 0)
print(numbers)    # [0, 1, 8, 5, 3]
```

✅ **ব্যবহার:**

* Priority Queue
* Efficient sorting
* Resource management

---

### 🟦 7. **Deque (ডাবল এন্ডেড কিউ)**

**ধারণা:**
Deque মানে Double Ended Queue — যেখানে দুই দিক থেকেই element যোগ বা বাদ দেওয়া যায়।

**উদাহরণ:**

```python
from collections import deque

dq = deque([10, 20, 30])
dq.appendleft(5)
dq.append(40)
print(dq)          # deque([5, 10, 20, 30, 40])
dq.pop()           # ডান দিক থেকে বাদ
dq.popleft()       # বাম দিক থেকে বাদ
```

✅ **ব্যবহার:**

* Palindrome checking
* Sliding window problem

---

### 🟩 8. **Priority Queue (প্রায়োরিটি কিউ)**

**ধারণা:**
এটি এমন একটি Queue যেখানে প্রতিটি element-এর সাথে একটি priority থাকে।
উচ্চ priority item আগে বের হয়।

**উদাহরণ:**

```python
import heapq

tasks = [(2, "low"), (1, "high"), (3, "very low")]
heapq.heapify(tasks)

while tasks:
    print(heapq.heappop(tasks))
```

✅ **ব্যবহার:**

* Task scheduling
* Operating System process management

---

## 🧩 সারসংক্ষেপ টেবিল:

| Data Structure | Type               | Order                 | Typical Use             |
| -------------- | ------------------ | --------------------- | ----------------------- |
| Stack          | LIFO               | Ordered               | Undo/Redo, Recursion    |
| Queue          | FIFO               | Ordered               | Task processing         |
| Linked List    | Sequential         | Ordered               | Dynamic storage         |
| Tree           | Hierarchical       | Partial order         | Search, hierarchy       |
| Graph          | Network            | Unordered             | Connection, path        |
| Heap           | Binary Tree        | Ordered (by priority) | Sorting, priority queue |
| Deque          | Double-ended queue | Ordered               | Palindrome check        |







# DAY-2
## **Python-এর “Slice” আর “Loop”** —
এই দুইটা জিনিস **Data Structure-এর প্রাণ** বলা যায় ❤️



## 🟩 **1. Slice (স্লাইস)**

**ধারণা:**
Slice মানে হচ্ছে কোনো **List**, **String**, বা **Tuple** থেকে নির্দিষ্ট অংশ (portion) কেটে নেওয়া।

---

### ✅ **সাধারণ সিনট্যাক্স:**

```python
sequence[start : end : step]
```

👉 যেখানে

* **start** = কোথা থেকে শুরু হবে
* **end** = কোথায় শেষ হবে (শেষ index ধরা হয় না)
* **step** = কত ধাপে চলবে (default = 1)

---

### 🧩 **উদাহরণ ১: List Slice**

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[1:4])      # index 1 থেকে 3 পর্যন্ত
print(numbers[:3])       # শুরু থেকে 3 এর আগ পর্যন্ত
print(numbers[3:])       # index 3 থেকে শেষ পর্যন্ত
print(numbers[::2])      # প্রতি ২ স্টেপ পর পর
print(numbers[::-1])     # উল্টা করে দেখাও (Reverse)
```

### 🧠 **আউটপুট:**

```
[20, 30, 40]
[10, 20, 30]
[40, 50, 60]
[10, 30, 50]
[60, 50, 40, 30, 20, 10]
```

---

### 🧩 **উদাহরণ ২: String Slice**

```python
name = "Python"

print(name[0:3])     # 'Pyt'
print(name[-3:])     # শেষের 3 অক্ষর ('hon')
print(name[::-1])    # উল্টো ('nohtyP')
```

---

### 🧠 **স্লাইসিং টিপস:**

| কাজ                 | সিনট্যাক্স | উদাহরণ                     |
| ------------------- | ---------- | -------------------------- |
| প্রথম ৩টা আইটেম     | `x[:3]`    | `[10, 20, 30]`             |
| শেষ ৩টা আইটেম       | `x[-3:]`   | `[40, 50, 60]`             |
| উল্টা করে দেখা      | `x[::-1]`  | `[60, 50, 40, 30, 20, 10]` |
| প্রতি ২টা বাদে দেখা | `x[::2]`   | `[10, 30, 50]`             |

---

## 🟨 **2. Loop (লুপ)**

**ধারণা:**
Loop মানে হলো — কোনো কাজ বারবার করা।
যতক্ষণ না কোনো শর্ত (condition) শেষ হয়।

---

### 🔹 **(a) for loop**

**ধারণা:**
কোনো sequence (list, tuple, string) এর উপর ঘুরে কাজ করে।

**উদাহরণ:**

```python
fruits = ["apple", "banana", "mango"]

for fruit in fruits:
    print(fruit)
```

**আউটপুট:**

```
apple
banana
mango
```

---

### 🔹 **(b) while loop**

**ধারণা:**
যতক্ষণ condition সত্য থাকে, ততক্ষণ লুপ চলবে।

**উদাহরণ:**

```python
count = 1
while count <= 5:
    print("Count:", count)
    count += 1
```

**আউটপুট:**

```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```

---

### 🔹 **(c) Loop এর সাথে range() ব্যবহার**

**range(start, end, step)** ব্যবহার করে সংখ্যা জেনারেট করা যায়।

**উদাহরণ:**

```python
for i in range(1, 6):
    print(i)
```

**আউটপুট:**

```
1
2
3
4
5
```

---

### 🔹 **(d) Nested Loop (লুপের ভিতরে লুপ)**

**উদাহরণ:**

```python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```

**আউটপুট:**

```
i=0, j=0
i=0, j=1
i=1, j=0
i=1, j=1
i=2, j=0
i=2, j=1
```

---

## 🧩 **Slice + Loop একসাথে ব্যবহার**

তুমি চাইলে Slice করে নেওয়া অংশের উপরও লুপ চালাতে পারো 👇

```python
numbers = [10, 20, 30, 40, 50]

for n in numbers[1:4]:     # index 1 থেকে 3 পর্যন্ত
    print("Number:", n)
```

**আউটপুট:**

```
Number: 20
Number: 30
Number: 40
```

---

## 🧠 **সারসংক্ষেপ:**

| বিষয়       | কাজ                                    | উদাহরণ                 |
| ---------- | -------------------------------------- | ---------------------- |
| Slice      | লিস্ট/স্ট্রিং-এর নির্দিষ্ট অংশ বের করা | `a[1:4]`, `name[::-1]` |
| for loop   | একাধিক আইটেমের উপর ঘুরে কাজ করা        | `for x in list:`       |
| while loop | যতক্ষণ condition সত্য, ততক্ষণ চলবে     | `while x < 5:`         |
| range()    | সংখ্যা জেনারেট করে                     | `range(1,10,2)`        |



## 🧠 **Control Flow (কন্ট্রোল ফ্লো) কী?**

Control Flow মানে হলো —
👉 প্রোগ্রামের কোড কোন ক্রমে (order এ) এক্সিকিউট হবে।

এটা নির্ভর করে তোমার দেওয়া **শর্ত (condition)**, **লুপ (loop)**, বা **ফাংশন কল (function call)**-এর উপর।

---

## 🟩 **1. Conditional Statements (শর্তাধীন স্টেটমেন্ট)**

Python-এ আমরা **if, elif, else** ব্যবহার করে শর্ত অনুযায়ী কোড চালাতে পারি।

---

### ✅ **(a) if স্টেটমেন্ট**

```python
x = 10
if x > 5:
    print("x 5 এর চেয়ে বড়")
```

🧠 আউটপুট:

```
x 5 এর চেয়ে বড়
```

---

### ✅ **(b) if-else স্টেটমেন্ট**

```python
x = 3
if x > 5:
    print("বড় সংখ্যা")
else:
    print("ছোট সংখ্যা")
```

🧠 আউটপুট:

```
ছোট সংখ্যা
```

---

### ✅ **(c) if-elif-else স্টেটমেন্ট**

```python
marks = 75

if marks >= 80:
    print("Grade: A+")
elif marks >= 70:
    print("Grade: A")
elif marks >= 60:
    print("Grade: A-")
else:
    print("Grade: Fail")
```

🧠 আউটপুট:

```
Grade: A
```

---

### ✅ **(d) Nested if (if এর ভিতরে if)**

```python
age = 20
gender = "male"

if age >= 18:
    if gender == "male":
        print("Adult male")
    else:
        print("Adult female")
```

🧠 আউটপুট:

```
Adult male
```

---

## 🟨 **2. Loop Statements (লুপ স্টেটমেন্ট)**

Control Flow-এর আরেকটি গুরুত্বপূর্ণ অংশ হলো **Loop**, যা একই কাজ বারবার করতে দেয়।

---

### ✅ **(a) for loop**

```python
for i in range(1, 6):
    print("Number:", i)
```

🧠 আউটপুট:

```
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5
```

---

### ✅ **(b) while loop**

```python
count = 1
while count <= 5:
    print("Count:", count)
    count += 1
```

🧠 আউটপুট:

```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```

---

## 🟥 **3. Loop Control Statements**

Loop-এর প্রবাহ (flow) নিয়ন্ত্রণ করতে কিছু বিশেষ স্টেটমেন্ট আছে 👇

---

### 🔹 **(a) break**

👉 লুপ বন্ধ করে দেয়।

```python
for i in range(1, 10):
    if i == 5:
        break
    print(i)
```

🧠 আউটপুট:

```
1
2
3
4
```

---

### 🔹 **(b) continue**

👉 বর্তমান iteration বাদ দিয়ে পরেরটিতে যায়।

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

🧠 আউটপুট:

```
1
2
4
5
```

---

### 🔹 **(c) pass**

👉 কিছু না করে শুধু জায়গা ধরে রাখে (placeholder হিসেবে ব্যবহৃত)।

```python
for i in range(5):
    if i == 2:
        pass
    print(i)
```

🧠 আউটপুট:

```
0
1
2
3
4
```

---

## 🟦 **4. Match Case (Python 3.10+)**

Python 3.10 থেকে নতুন **match-case** সিনট্যাক্স এসেছে, যেটা switch-case এর মতো কাজ করে।

```python
command = "start"

match command:
    case "start":
        print("System starting...")
    case "stop":
        print("System stopping...")
    case _:
        print("Unknown command")
```

🧠 আউটপুট:

```
System starting...
```

---

## 🧩 **সারসংক্ষেপ টেবিল:**

| অংশ          | কাজ                               | উদাহরণ               |
| ------------ | --------------------------------- | -------------------- |
| if           | শর্ত সত্য হলে কোড চালায়          | `if x > 0:`          |
| if-else      | শর্ত অনুযায়ী দুই দিক             | `if...else`          |
| if-elif-else | একাধিক শর্ত                       | `elif`               |
| for loop     | নির্দিষ্ট সংখ্যা বা তালিকায় ঘোরে | `for i in range(5):` |
| while loop   | শর্ত সত্য থাকা পর্যন্ত ঘোরে       | `while x < 5:`       |
| break        | লুপ বন্ধ করে                      | `break`              |
| continue     | iteration স্কিপ করে               | `continue`           |
| pass         | কিছু না করে                       | `pass`               |
| match-case   | switch-case এর মতো                | `match variable:`    |



# Day-3


## 🧵 String (স্ট্রিং) কী?

**String** হলো এমন একটি ডেটা টাইপ যেখানে **অক্ষর, সংখ্যা বা চিহ্ন** একসাথে থাকে — সাধারণত **উদ্ধৃতি চিহ্নের (" " বা ' ')** মধ্যে।

### 🎯 উদাহরণ:

```python
name = "Mamun"
message = 'Hello, World!'
```

🔹 এখানে `name` এবং `message` দুটোই **string**।

---

## 🧠 স্ট্রিং-এর কিছু বৈশিষ্ট্য

1️⃣ স্ট্রিং হলো **characters-এর একটা ক্রম (sequence)**।
2️⃣ স্ট্রিং-এর প্রতিটি অক্ষরের একটা **index number** থাকে।
3️⃣ Python-এ স্ট্রিং **immutable** — অর্থাৎ তৈরি হওয়ার পর এর ভেতরের মান পরিবর্তন করা যায় না।

---

## 🔢 Indexing (ইনডেক্সিং)

**Indexing** মানে হলো — স্ট্রিংয়ের নির্দিষ্ট পজিশনের অক্ষরটিকে বের করা।

👉 Python-এ **ইনডেক্স ০ (zero)** থেকে শুরু হয়।

### 🎯 উদাহরণ:

```python
name = "Python"
print(name[0])  # P
print(name[1])  # y
print(name[5])  # n
```

🔹 এখানে

* `name[0]` → প্রথম অক্ষর `'P'`
* `name[5]` → ষষ্ঠ অক্ষর `'n'`

---

## 🔙 Negative Indexing (নেগেটিভ ইনডেক্সিং)

আপনি চাইলে **শেষ দিক থেকেও** ইনডেক্স দিতে পারেন, `-1` থেকে শুরু করে।

```python
word = "Python"
print(word[-1])  # n
print(word[-2])  # o
```

➡️ `-1` মানে শেষ অক্ষর, `-2` মানে শেষের আগের অক্ষর।

---

## ✂️ Slicing (স্লাইসিং)

**Slicing** মানে হলো — স্ট্রিংয়ের নির্দিষ্ট অংশ কেটে নেওয়া।

👉 সিনট্যাক্স:

```python
string[start:end]
```

(এখানে `start` ইনডেক্স থেকে শুরু হবে, কিন্তু `end` ইনডেক্সের আগ পর্যন্ত যাবে।)

### 🎯 উদাহরণ:

```python
name = "Python"
print(name[0:4])  # Pyth
print(name[2:6])  # thon
```

🔹 ব্যাখ্যা:

* `name[0:4]` → ইনডেক্স ০ থেকে শুরু, কিন্তু ৪-এর আগ পর্যন্ত যাবে।
* তাই ফলাফল `'Pyth'`।

---

## 🚀 Step সহ Slicing

স্লাইসিং-এ আপনি **step value** দিতে পারেন — অর্থাৎ কয় ধাপে অক্ষর নেওয়া হবে।

👉 সিনট্যাক্স:

```python
string[start:end:step]
```

### 🎯 উদাহরণ:

```python
name = "Python"
print(name[0:6:2])  # Pto
```

➡️ ইনডেক্স ০ থেকে ৬ পর্যন্ত, কিন্তু প্রতি ২ ধাপে অক্ষর নেয়।

---

## 🔄 String Reverse করা

স্টেপ হিসেবে `-1` দিলে স্ট্রিং উল্টো হয়ে যায়।

```python
text = "Python"
print(text[::-1])  # nohtyP
```

---

## 🧩 কিছু দরকারি উদাহরণ

```python
word = "Programming"
print(word[:6])    # Progra
print(word[3:])    # gramming
print(word[-4:])   # ming
print(word[::3])   # Pgai
```

---

## 🎯 প্র্যাকটিস এক্সারসাইজ

1️⃣ কোনো স্ট্রিং ইনপুট নিয়ে প্রথম ও শেষ অক্ষর প্রিন্ট করো।
2️⃣ `"Python"` থেকে `"yth"` অংশটা বের করো স্লাইসিং ব্যবহার করে।
3️⃣ ব্যবহারকারীর দেওয়া কোনো নাম উল্টো করে প্রিন্ট করো।
4️⃣ `"Programming"` স্ট্রিং থেকে `"gram"` অংশটা বের করো।
5️⃣ `"Bangladesh"` থেকে প্রতি দ্বিতীয় অক্ষর প্রিন্ট করো।



## 🧠 String Method কী?

**String Methods** হলো কিছু **বিল্ট-ইন ফাংশন (built-in functions)** যেগুলো স্ট্রিং-এর উপর ব্যবহার করে সহজে কাজ করা যায় — যেমন বড় হাতের অক্ষরে করা, ছোট হাতের অক্ষরে করা, কোনো শব্দ খোঁজা, পরিবর্তন করা ইত্যাদি।

👉 উদাহরণ:

```python
name = "mamun"
print(name.upper())   # Output: MAMUN
```

---

## 🧩 সাধারণত ব্যবহৃত String Methods

| মেথড                    | কাজ                                                 | উদাহরণ                                                        |
| ----------------------- | --------------------------------------------------- | ------------------------------------------------------------- |
| **upper()**             | সব অক্ষরকে বড় হাতের করে                             | `"python".upper()` → `'PYTHON'`                               |
| **lower()**             | সব অক্ষরকে ছোট হাতের করে                            | `"PYTHON".lower()` → `'python'`                               |
| **title()**             | প্রতিটি শব্দের প্রথম অক্ষর বড় করে                   | `"hello world".title()` → `'Hello World'`                     |
| **capitalize()**        | শুধু প্রথম অক্ষর বড় করে                             | `"python".capitalize()` → `'Python'`                          |
| **strip()**             | শুরু ও শেষের ফাঁকা জায়গা মুছে দেয়                   | `"  hello  ".strip()` → `'hello'`                             |
| **lstrip() / rstrip()** | বাম/ডান দিকের ফাঁকা জায়গা মুছে দেয়                  | `"  hi ".lstrip()` → `'hi '`                                  |
| **replace(old, new)**   | কোনো শব্দ বা অক্ষর পরিবর্তন করে                     | `"I like Java".replace("Java", "Python")` → `'I like Python'` |
| **split()**             | স্ট্রিংকে ভেঙে লিস্ট বানায়                          | `"a,b,c".split(",")` → `['a', 'b', 'c']`                      |
| **join()**              | লিস্টকে একত্র করে স্ট্রিং বানায়                     | `",".join(['a','b','c'])` → `'a,b,c'`                         |
| **find()**              | কোনো অক্ষর বা শব্দের ইনডেক্স খুঁজে দেয় (না পেলে -1) | `"Hello".find("e")` → `1`                                     |
| **count()**             | কোনো অক্ষর বা শব্দ কয়বার আছে গুনে                   | `"banana".count("a")` → `3`                                   |
| **startswith()**        | কোনো স্ট্রিং নির্দিষ্ট শব্দ দিয়ে শুরু হয়েছে কি না   | `"Python".startswith("Py")` → `True`                          |
| **endswith()**          | কোনো স্ট্রিং নির্দিষ্ট শব্দে শেষ হয়েছে কি না        | `"Python".endswith("on")` → `True`                            |
| **isdigit()**           | স্ট্রিং-এ সব সংখ্যা আছে কি না                       | `"123".isdigit()` → `True`                                    |
| **isalpha()**           | স্ট্রিং-এ সব অক্ষর আছে কি না                        | `"abc".isalpha()` → `True`                                    |
| **isalnum()**           | স্ট্রিং-এ শুধু অক্ষর ও সংখ্যা আছে কি না             | `"abc123".isalnum()` → `True`                                 |
| **swapcase()**          | ছোট-বড় হাতের অক্ষর উল্টে দেয়                        | `"PyThOn".swapcase()` → `'pYtHoN'`                            |

---

## 🧾 উদাহরণ ১:

```python
name = "   Hello Python   "
print(name.strip())          # "Hello Python"
print(name.upper())          # "   HELLO PYTHON   "
print(name.lower())          # "   hello python   "
```

---

## 🧾 উদাহরণ ২:

```python
text = "I love programming in Python"
print(text.replace("Python", "Java"))
print(text.find("programming"))
print(text.count("o"))
```

➡️ Output:

```
I love programming in Java  
7  
3
```

---

## 🧾 উদাহরণ ৩:

```python
sentence = "learn python programming"
print(sentence.title())   # Learn Python Programming
print(sentence.capitalize())  # Learn python programming
```

---

## 🧾 উদাহরণ ৪:

```python
data = "apple,banana,mango"
fruits = data.split(",")
print(fruits)
print("-".join(fruits))
```

➡️ Output:

```
['apple', 'banana', 'mango']
apple-banana-mango
```

---

## 🎯 প্র্যাকটিস এক্সারসাইজ

1️⃣ কোনো নাম ইনপুট নিয়ে বড় হাতের ও ছোট হাতের দুইভাবে প্রিন্ট করো।
2️⃣ `"I love Python"` স্ট্রিং-এ “Python” কে “Programming” দিয়ে replace করো।
3️⃣ ব্যবহারকারীর দেওয়া স্ট্রিং-এ কয়টা `'a'` আছে তা বের করো।
4️⃣ `"Hello World"` স্ট্রিংটি উল্টে দাও এবং প্রথম অক্ষর ক্যাপিটাল করো।
5️⃣ একটি বাক্য ইনপুট নিয়ে সেটাকে লিস্টে পরিণত করো (`split()` ব্যবহার করে) এবং পুনরায় স্ট্রিং বানাও (`join()` দিয়ে)।




## 🧵 String Splitting (স্ট্রিং ভাঙা)

**Splitting** মানে হলো একটি বড় স্ট্রিংকে **ছোট ছোট অংশে ভাগ করা**।
Python-এ এটা করার জন্য আমরা ব্যবহার করি 👉 **`split()`** মেথড।

---

### 🎯 উদাহরণ:

```python
text = "apple,banana,mango"
fruits = text.split(",")
print(fruits)
```

➡️ Output:

```
['apple', 'banana', 'mango']
```

🔹 ব্যাখ্যা:

* `split(",")` মানে হলো কমা `,` দিয়ে স্ট্রিংটি ভাগ করো।
* ফলাফল হিসেবে একটা **list** পাওয়া যায়।

---

### ⚙️ Default Split (স্পেস দিয়ে ভাঙা)

যদি কিছু না দেন, তাহলে `split()` ডিফল্টভাবে **space** দিয়ে ভাগ করে।

```python
sentence = "I love Python programming"
print(sentence.split())
```

➡️ Output:

```
['I', 'love', 'Python', 'programming']
```

---

## 🔗 String Joining (স্ট্রিং যুক্ত করা)

**Joining** মানে হলো — একটি **list-এর সব উপাদান একত্রে জোড়া লাগানো**, এবং মাঝখানে আপনি নির্দিষ্ট কোনো চিহ্ন দিতে পারেন।

👉 সিনট্যাক্স:

```python
'separator'.join(list)
```

---

### 🎯 উদাহরণ:

```python
fruits = ['apple', 'banana', 'mango']
text = ", ".join(fruits)
print(text)
```

➡️ Output:

```
apple, banana, mango
```

🔹 এখানে `", ".join(fruits)` মানে — লিস্টের প্রতিটি উপাদানের মাঝে কমা ও স্পেস বসিয়ে একত্র করা হয়েছে।

---

### ⚙️ আরেকটি উদাহরণ:

```python
words = ['Python', 'is', 'fun']
print(" ".join(words))
```

➡️ Output:

```
Python is fun
```

---

## ✨ String Formatting (স্ট্রিং সাজানো বা মান বসানো)

**String Formatting** মানে হলো — স্ট্রিংয়ের মধ্যে **ভেরিয়েবলের মান যুক্ত করে সুন্দরভাবে দেখানো**।

Python-এ এটা করার তিনটি জনপ্রিয় পদ্ধতি আছে 👇

---

### 🧩 ১️⃣ f-string (সবচেয়ে আধুনিক ও সহজ)

```python
name = "Mamun"
age = 25
print(f"My name is {name} and I am {age} years old.")
```

➡️ Output:

```
My name is Mamun and I am 25 years old.
```

---

### 🧩 ২️⃣ format() মেথড

```python
name = "Mamun"
age = 25
print("My name is {} and I am {} years old.".format(name, age))
```

➡️ Output:

```
My name is Mamun and I am 25 years old.
```

🔹 চাইলে পজিশনও নির্ধারণ করতে পারেন:

```python
print("My name is {1} and I am {0} years old.".format(age, name))
```

➡️ Output:

```
My name is Mamun and I am 25 years old.
```

---

### 🧩 ৩️⃣ পুরনো `%` ফরম্যাটিং (C স্টাইল)

```python
name = "Mamun"
age = 25
print("My name is %s and I am %d years old." % (name, age))
```

➡️ Output:

```
My name is Mamun and I am 25 years old.
```

🔹 `%s` → string, `%d` → integer, `%f` → float

---

## 🧾 অতিরিক্ত উদাহরণ

```python
price = 49.99
print(f"The price is {price:.2f}")   # দুই ঘর পর্যন্ত দশমিক দেখাবে
```

➡️ Output:

```
The price is 49.99
```

---

## 🎯 প্র্যাকটিস এক্সারসাইজ

1️⃣ `"apple,banana,mango"` স্ট্রিংটি ভেঙে লিস্টে রাখো, তারপর আবার কমা দিয়ে যুক্ত করো।
2️⃣ ব্যবহারকারীর কাছ থেকে নাম ও বয়স ইনপুট নিয়ে f-string ব্যবহার করে সুন্দরভাবে প্রিন্ট করো।
3️⃣ `"I love Python programming"` স্ট্রিংটি শব্দভাগে ভেঙে প্রতিটি শব্দ আলাদা লাইনে প্রিন্ট করো।
4️⃣ `"Bangladesh is beautiful"` স্ট্রিংটিকে `"-"` দিয়ে যুক্ত করো।
5️⃣ কোনো প্রোডাক্টের নাম ও দাম ফরম্যাট করে দেখাও:

```
Product: Laptop | Price: $550.00
```



## 🧠 **Comprehension মানে কী?**

**Comprehension** শব্দের মানে হলো “সহজভাবে তৈরি করা” বা “সহজভাবে বোঝা।”
Python-এ **Comprehension** মানে হচ্ছে —
একটি নতুন **list**, **set**, **dictionary**, বা **generator** তৈরি করার **সংক্ষিপ্ত ও সুন্দর পদ্ধতি**,
যেখানে লুপ (loop) আর শর্ত (condition) একসাথে এক লাইনে ব্যবহার করা যায়।

---

## 🔹 **Python-এ ৪ ধরনের Comprehension আছে**

| ধরন                          | কী তৈরি করে                 | উদাহরণ                       |
| ---------------------------- | --------------------------- | ---------------------------- |
| **List Comprehension**       | List                        | `[x for x in range(5)]`      |
| **Set Comprehension**        | Set                         | `{x for x in range(5)}`      |
| **Dictionary Comprehension** | Dictionary                  | `{x: x*x for x in range(5)}` |
| **Generator Comprehension**  | Generator (iterable object) | `(x for x in range(5))`      |

---

## 🟩 **1️⃣ List Comprehension**

👉 এক লাইনে লুপ চালিয়ে লিস্ট তৈরি করা।

```python
numbers = [1, 2, 3, 4, 5]
squares = [n*n for n in numbers]
print(squares)
```

🧠 আউটপুট:

```
[1, 4, 9, 16, 25]
```

🎯 ব্যাখ্যা:

* প্রতিটি `n` এর মান নিয়ে তার বর্গ `n*n` করা হচ্ছে
* এবং সেই মান লিস্টে যুক্ত হচ্ছে

---

## 🟨 **2️⃣ Set Comprehension**

👉 লিস্টের মতো, তবে **duplicate value** রাখে না।

```python
numbers = [1, 2, 2, 3, 4, 4]
unique = {n for n in numbers}
print(unique)
```

🧠 আউটপুট:

```
{1, 2, 3, 4}
```

🎯 ব্যাখ্যা:

* `{}` ব্যবহার করলে সেট তৈরি হয়
* একই মান বারবার থাকলে শুধু একবারই থাকবে

---

## 🟦 **3️⃣ Dictionary Comprehension**

👉 একসাথে **key-value pair** তৈরি করতে কাজে লাগে।

```python
squares = {n: n*n for n in range(1, 6)}
print(squares)
```

🧠 আউটপুট:

```
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

🎯 ব্যাখ্যা:

* প্রতিটি `n` এর key হচ্ছে `n`
* value হচ্ছে তার square (`n*n`)

---

## 🟧 **4️⃣ Generator Comprehension**

👉 লিস্টের মতোই, কিন্তু **memory-efficient** কারণ এটি মানগুলো **একটার পর একটা তৈরি করে**।

```python
gen = (n*n for n in range(5))
for i in gen:
    print(i)
```

🧠 আউটপুট:

```
0
1
4
9
16
```

🎯 ব্যাখ্যা:

* এখানে লিস্টের মতো একসাথে সব মান মেমোরিতে রাখে না
* প্রয়োজনে মানগুলো তৈরি করে দেয় (lazy evaluation)

---

## ⚙️ **Comprehension-এর মূল সুবিধা**

| সুবিধা                | ব্যাখ্যা                           |
| --------------------- | ---------------------------------- |
| ✅ কোড ছোট হয়          | লুপ, append, condition সব এক লাইনে |
| ✅ পড়তে সহজ            | এক নজরে বোঝা যায় কী হচ্ছে          |
| ✅ পারফরম্যান্স ভালো   | কিছু ক্ষেত্রে লুপের চেয়ে দ্রুত     |
| ✅ সহজে filter করা যায় | `if` ব্যবহার করে শর্ত বসানো যায়    |

---

## 🧩 **উদাহরণ: If সহ List Comprehension**

```python
even_numbers = [x for x in range(10) if x % 2 == 0]
print(even_numbers)
```

🧠 আউটপুট:

```
[0, 2, 4, 6, 8]
```

🎯 এখানে:

* লুপ ঘুরছে `range(10)` এর ওপর
* `if x % 2 == 0` মানে শুধু even সংখ্যাগুলোই নেওয়া হচ্ছে

---

## 🧠 সারসংক্ষেপে:

| Comprehension টাইপ | কাজ            | ব্র্যাকেট      |
| ------------------ | -------------- | -------------- |
| List               | লিস্ট তৈরি     | `[]`           |
| Set                | সেট তৈরি       | `{}`           |
| Dictionary         | key-value জোড়া | `{key: value}` |
| Generator          | মান yield করে  | `()`           |





## 🧠 **List Comprehension কী?**

**List Comprehension** হলো — লুপ (loop) এবং কন্ডিশন (if) ব্যবহার করে
এক লাইনে নতুন **list তৈরি করার শর্টকাট** পদ্ধতি।

---

### 🎯 **সাধারণ সিনট্যাক্স:**

```python
[expression for item in iterable if condition]
```

👉 অর্থাৎ

* **expression:** কী রাখবে (যেমন x বা x*2)
* **item:** লুপের প্রতিটি মান
* **iterable:** যেমন list, range, string
* **condition (ঐচ্ছিক):** কোন শর্তে রাখবে

---

## 🟩 **1️⃣ সাধারণ উদাহরণ**

```python
numbers = [1, 2, 3, 4, 5]
squares = [n * n for n in numbers]
print(squares)
```

🧠 **আউটপুট:**

```
[1, 4, 9, 16, 25]
```

👉 ব্যাখ্যা:
for লুপ দিয়ে ঘুরে প্রতিটি সংখ্যার বর্গ (square) নতুন লিস্টে রাখছে।

---

## 🟨 **2️⃣ if সহ List Comprehension (Control Flow inside)**

```python
numbers = [1, 2, 3, 4, 5, 6]
even_numbers = [n for n in numbers if n % 2 == 0]
print(even_numbers)
```

🧠 **আউটপুট:**

```
[2, 4, 6]
```

👉 ব্যাখ্যা:
`if n % 2 == 0` মানে শুধুমাত্র জোড় সংখ্যা নেবে।

---

## 🟦 **3️⃣ if-else সহ List Comprehension**

তুমি চাইলে একসাথে **if-else** ব্যবহার করেও কোড লিখতে পারো।

```python
numbers = [1, 2, 3, 4, 5]
result = ["even" if n % 2 == 0 else "odd" for n in numbers]
print(result)
```

🧠 **আউটপুট:**

```
['odd', 'even', 'odd', 'even', 'odd']
```

👉 ব্যাখ্যা:
প্রতিটি সংখ্যার জন্য চেক করছে — even হলে "even", নাহলে "odd" লিখছে।

---

## 🟥 **4️⃣ Nested Loop (লুপের ভিতরে লুপ)**

List comprehension-এর মধ্যে একাধিক লুপও দেওয়া যায় 👇

```python
pairs = [(x, y) for x in [1, 2, 3] for y in [4, 5]]
print(pairs)
```

🧠 **আউটপুট:**

```
[(1, 4), (1, 5), (2, 4), (2, 5), (3, 4), (3, 5)]
```

👉 ব্যাখ্যা:
প্রতিটি `x` এর সাথে প্রতিটি `y` মিলিয়ে tuple তৈরি করছে।

---

## 🟪 **5️⃣ Nested if সহ List Comprehension**

```python
numbers = [10, 15, 20, 25, 30]
filtered = [n for n in numbers if n > 15 if n % 5 == 0]
print(filtered)
```

🧠 **আউটপুট:**

```
[20, 25, 30]
```

👉 ব্যাখ্যা:
একাধিক শর্ত ব্যবহার করা হয়েছে:

* 15 এর চেয়ে বড়
* 5 দিয়ে বিভাজ্য

---

## 🟫 **6️⃣ String List Comprehension**

```python
name = "Python"
letters = [ch for ch in name]
print(letters)
```

🧠 **আউটপুট:**

```
['P', 'y', 't', 'h', 'o', 'n']
```

---

## 🧩 **Control Flow Logic Summary**

| ধরণ         | কাজ                       | উদাহরণ                                        |
| ----------- | ------------------------- | --------------------------------------------- |
| সাধারণ      | লুপের ফলাফল রাখে          | `[x*2 for x in list]`                         |
| if          | শর্ত দিয়ে ফিল্টার করে     | `[x for x in list if x>10]`                   |
| if-else     | শর্ত অনুযায়ী মান নির্ধারণ | `["even" if x%2==0 else "odd" for x in list]` |
| nested loop | একাধিক লুপ একসাথে         | `[(x,y) for x in A for y in B]`               |
| nested if   | একাধিক শর্ত               | `[x for x in list if x>5 if x<20]`            |

---

## 🧠 **List Comprehension বনাম সাধারণ for loop**

### 🔹 সাধারণ for loop:

```python
result = []
for n in range(1, 6):
    result.append(n * 2)
```

### 🔹 List comprehension:

```python
result = [n * 2 for n in range(1, 6)]
```

🟢 **একই কাজ, কিন্তু অনেক ছোট ও পরিষ্কার!**

---

## 🧮 **Mini Practice Example**

1️⃣ ১ থেকে ২০ পর্যন্ত **জোড় সংখ্যা** এর লিস্ট বানাও
2️⃣ ১ থেকে ২০ পর্যন্ত সংখ্যার মধ্যে শুধুমাত্র **৩ ও ৫ দিয়ে বিভাজ্য** সংখ্যাগুলো রাখো
3️⃣ একটি স্ট্রিং থেকে **স্বরবর্ণ (vowels)** গুলো লিস্টে রাখো



## ⚙️ **Generator কী?**

👉 **Generator** হলো এমন এক ধরনের **iterator**,
যা একসাথে পুরো ডেটা মেমোরিতে না রেখে,
**একটা একটা করে মান তৈরি করে দেয় (on demand)**।

অর্থাৎ, তুমি যখন মান চাও, তখনই সেটা বানায় —
আগে থেকে সব বানিয়ে মেমোরি ভর্তি করে না।

---

### 📦 **সাধারণ লিস্ট বনাম জেনারেটর**

| বিষয়           | List                | Generator          |
| -------------- | ------------------- | ------------------ |
| মান তৈরি       | সব একসাথে           | একটার পর একটা      |
| মেমোরি ব্যবহার | বেশি                | খুব কম             |
| গতিবেগ         | দ্রুত ছোট dataset এ | বড় dataset এ দ্রুত |
| Syntax         | `[]`                | `()`               |

---

## 🧩 **একটি সহজ উদাহরণ:**

### 🔹 লিস্ট কম্প্রিহেনশন:

```python
nums = [x*x for x in range(5)]
print(nums)
```

🧠 আউটপুট:

```
[0, 1, 4, 9, 16]
```

➡️ এখানে একসাথে পুরো লিস্ট তৈরি হচ্ছে।

---

### 🔹 Generator Comprehension:

```python
nums = (x*x for x in range(5))
print(nums)
```

🧠 আউটপুট:

```
<generator object <genexpr> at 0x0000023B6D...>
```

👉 মানে, এটা লিস্ট না — বরং **generator object**।

তুমি এখন একটার পর একটা মান পেতে পারবে 👇

```python
for n in nums:
    print(n)
```

🧠 আউটপুট:

```
0
1
4
9
16
```

---

## 🧠 **Generator Function**

Generator শুধু comprehension দিয়েই হয় না —
**function দিয়েও বানানো যায়** `yield` কীওয়ার্ড ব্যবহার করে।

---

### 🔹 সাধারণ function (return):

```python
def normal_func():
    return [1, 2, 3]
```

👉 একসাথে সব মান ফেরত দেয়।

---

### 🔹 Generator function (yield):

```python
def gen_func():
    for i in range(1, 4):
        yield i
```

🧠 ব্যবহার:

```python
for num in gen_func():
    print(num)
```

আউটপুট:

```
1
2
3
```

🎯 এখানে `yield` মানে —

> “এই মানটা দাও, তারপর থেমে থাকো — পরেরবার আবার এখান থেকেই শুরু করো।”

---

## 🧮 **Generator কীভাবে কাজ করে (step by step)**

ধরো, নিচের কোডটা দেখি 👇

```python
def count_up_to(n):
    count = 1
    while count <= n:
        yield count
        count += 1

counter = count_up_to(5)
```

এখন `counter` হলো generator object।

তুমি চাইলে একটার পর একটা মান নিতে পারবে:

```python
print(next(counter))  # 1
print(next(counter))  # 2
print(next(counter))  # 3
```

যতক্ষণ পর্যন্ত মান আছে ততক্ষণ `next()` কাজ করবে,
শেষ হলে **StopIteration** error দিবে।

---

## 🧠 **Generator কেন দরকার?**

| কারণ                                 | ব্যাখ্যা                        |
| ------------------------------------ | ------------------------------- |
| ✅ **Memory-efficient**               | একসাথে সব ডেটা মেমোরিতে রাখে না |
| ✅ **Fast for large data**            | বড় ডেটাসেটে ভালো কাজ করে        |
| ✅ **Infinite sequence তৈরি করা যায়** | যেমন Fibonacci সিরিজ            |
| ✅ **Lazy Evaluation**                | প্রয়োজন হলে তখনই মান তৈরি হয়    |

---

## 🧩 **উদাহরণ: Fibonacci Generator**

```python
def fibonacci(limit):
    a, b = 0, 1
    while a < limit:
        yield a
        a, b = b, a + b

for num in fibonacci(10):
    print(num)
```

🧠 আউটপুট:

```
0
1
1
2
3
5
8
```

---

## 🧾 সারসংক্ষেপ:

| বিষয়               | Generator                 | Function             |
| ------------------ | ------------------------- | -------------------- |
| কীওয়ার্ড           | `yield`                   | `return`             |
| মান তৈরি           | একটার পর একটা             | একসাথে সব            |
| Memory             | খুব কম লাগে               | বেশি লাগে            |
| State মনে রাখে     | হ্যাঁ                     | না                   |
| ব্যবহারের উদ্দেশ্য | বড় dataset বা stream data | ছোট বা নির্দিষ্ট কাজ |


