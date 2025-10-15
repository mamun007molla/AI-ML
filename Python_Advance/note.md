# 🚀 Function কী? (একদম সহজভাবে শিখি)

**Function** হলো এমন একটি কোড ব্লক যা নির্দিষ্ট কোনো কাজ করার জন্য বানানো হয়।
👉 সহজ কথায়: **বারবার একই কোড লিখতে না হয়ে, একবার লিখে অনেকবার ব্যবহার করা যায় — এটিই Function।**

---

### 🎯 কেন Function ব্যবহার করবো?

| সুবিধা          | ব্যাখ্যা                                      |
| --------------- | --------------------------------------------- |
| ✅ কোড ছোট হয়    | একই কোড বারবার লিখতে হয় না                    |
| ✅ Reusable      | একবার function লিখে অনেকবার ব্যবহার করা যায়   |
| ✅ সহজে বুঝা যায় | প্রোগ্রাম clean এবং readable হয়               |
| ✅ Debugging সহজ | সমস্যা হলে শুধু function অংশ পরীক্ষা করলেই হয় |

---

### 💡 Real Life Example

তুমি যদি প্রতিদিন চা বানাও — **চা বানানোর নিয়মটা একটা function-এর মতো**

* পানি গরম করো
* চা-পাতি দাও
* চিনি দাও
* পরিবেশন করো

👉 **একই স্টেপ প্রতিদিন করছো — মানে তুমি এক ধরনের function চালাচ্ছো!**

---

### 🧠 Python-এ Function কীভাবে লিখি?

```python
def hello():
    print("Hello, Python!")
```

👉 এখানে:

* `def` → function শুরু করার কীওয়ার্ড
* `hello()` → function-এর নাম
* `print(...)` → কাজ যা করবে
* **Call না করলে function কিছুই রান করবে না**

### 🔁 Function Call

```python
hello()  # Output হবে → Hello, Python!
```

---

### 🎁 Full Example:

```python
def greet():
    print("Welcome, user!")

# Function call
greet()
```

---

### 🎯 এক লাইনে মনে রাখো:

> **Function = কোডকে ছোট ছোট reusable অংশে ভাগ করার স্মার্ট উপায়।**

---

দারুণ! এখন আমরা **Function with Parameters & Return Value** শিখবো। এটা বুঝলে তুমি নিজের মতো করে **smart function বানাতে পারবে — যেমন ক্যালকুলেটর, মার্কশিট সিস্টেম, ATM সিমুলেশন ইত্যাদি।**

---

## 🎯 Function with Parameters (Argument সহ Function)

👉 Parameter মানে হলো **function-এ ডেটা দেওয়া**, যেন সে সেটা নিয়ে কাজ করতে পারে।

```python
def greet(name):   # এখানে name হলো parameter
    print("Hello,", name)

greet("Rahim")   # এখানে "Rahim" হলো argument (real value)
```

✅ Output:

```
Hello, Rahim
```

---

## 🎯 Function with Multiple Parameters

```python
def add(a, b):
    print(a + b)

add(5, 10)   # Output: 15
```

✅ Function input নিয়ে কাজ করলো।

---

## 🔄 Return Value সহ Function (ফলাফল ফেরত দেয়)

👉 কখনো কখনো শুধু print করলে হবে না। **ফলাফল ধরে রাখতে চাইলে return ব্যবহার করতে হয়।**

```python
def add(a, b):
    return a + b   # ফলাফল ফেরত দিলো

result = add(10, 20)
print("Result:", result)
```

✅ Output:

```
Result: 30
```

---

## 🔥 Print vs Return — পার্থক্য বোঝো

| বিষয়                   | `print()`  | `return`                       |
| ---------------------- | ---------- | ------------------------------ |
| কাজ                    | শুধু দেখায় | ফলাফল ধরে রাখতে দেয়            |
| পুনরায় ব্যবহার         | ❌ না       | ✅ হ্যাঁ                        |
| Function শেষ করে ফেলে? | ❌ না       | ✅ return হলে function থেমে যায় |

---

## 💡 Example: Marksheet Calculation Function

```python
def calculate_total(marks1, marks2, marks3):
    total = marks1 + marks2 + marks3
    return total

total_marks = calculate_total(80, 75, 90)
print("Total Marks:", total_marks)
```

---

### 🎯 এক লাইনে মনে রাখো:

> **Parameter = ডেটা ইনপুট | Return = ফলাফল আউটপুট**

---


## ✅ 1. Default Parameter (মান না দিলেও Function কাজ করবে)

👉 যদি ইউজার আর্গুমেন্ট না দেয়, তাহলে **ডিফল্ট মান** ব্যবহার হবে।

```python
def greet(name="User"):
    print("Hello,", name)

greet("Rahim")   # Output: Hello, Rahim
greet()          # Output: Hello, User (default value ব্যবহার হলো)
```

🎯 ব্যবহার হয় যখন **মান optional হয়**।

---

## ✅ 2. Keyword Arguments (যে কোনো ক্রমে মান দেওয়া যায়)

👉 তোমাকে মান **strict order** এ দিতে হবে না — **Key দিয়ে দিলে Python নিজে বুঝে নেবে।**

```python
def profile(name, age, city):
    print(name, age, city)

profile(age=25, city="Dhaka", name="Karim")  # Order উল্টা হলেও সমস্যা নেই
```

🎉 Output → `Karim 25 Dhaka`

---

## ✅ 3. *args → একাধিক মান (Unlimited Arguments - Tuple আকারে ধরে)

👉 যখন **কতগুলো মান আসবে জানা নেই**, তখন ব্যবহার করো।

```python
def total(*numbers):
    print(sum(numbers))

total(10, 20, 30, 40)  # output: 100
```

➡ `*args` সব মানকে **tuple করে নেয়**

---

## ✅ 4. **kwargs → Many Arguments, but as Key:Value (Dictionary আকারে ধরে)

👉 অনেক Named Argument নিতে চাইলে:

```python
def details(**info):
    print(info)

details(name="Rahim", age=22, city="Dhaka")
# Output: {'name': 'Rahim', 'age': 22, 'city': 'Dhaka'}
```

➡ `**kwargs` সব মানকে **dictionary করে নেয়**

---

### 🎯 Summary Table

| Topic             | Syntax          | Data Format | Use Case             |
| ----------------- | --------------- | ----------- | -------------------- |
| Default Parameter | `def f(a=10)`   | -           | Optional মান দিতে    |
| Keyword Argument  | `f(a=10, b=20)` | -           | Order free arguments |
| `*args`           | `def f(*x)`     | Tuple       | Unlimited মান        |
| `**kwargs`        | `def f(**x)`    | Dictionary  | Unlimited key-value  |

---

নিশ্চিত! এখন আমি **Iterator ও Generator** নিয়ে তুমি যেসব প্রশ্ন করেছো এবং আমি যেসব উত্তর দিয়েছি—সবকিছু **একসাথে পরিষ্কারভাবে, সহজ ভাষায়** সাজিয়ে দিচ্ছি যাতে তোমার **সম্পূর্ণ ধারণা ক্লিয়ার হয় এবং মনে থাকে।** 🚀

---

## 🎯 ১. Iterator কী?

✅ **Iterator = এমন অবজেক্ট যাকে থেকে একটার পর একটা করে মান নেওয়া যায় (`next()`)**

👉 Iterator তৈরি করতে: `iter()`
👉 পরবর্তী মান নিতে: `next()`

```python
numbers = [10, 20, 30]
it = iter(numbers)

print(next(it))  # 10
print(next(it))  # 20
print(next(it))  # 30
```

➡ `next()` শেষ হলে → `StopIteration` Error দেয়।

---

## ⚙ `for` লoop আসলে কিভাবে কাজ করে?

➡ **Python inside এ করে**:

```python
it = iter(numbers)
while True:
    print(next(it))
```

👉 তাই **Iterator = For loop এর backend system**

---

## 🎯 ২. Generator কী?

✅ **Generator হলো iterator তৈরি করার সবচেয়ে সহজ উপায়।**

👉 সাধারণ function এ `return` থাকে
👉 Generator function এ `yield` থাকে (**এটা return + pause system**)

```python
def gen_numbers():
    yield 1
    yield 2
    yield 3

g = gen_numbers()
print(next(g))  # 1
print(next(g))  # 2
```

---

## 🔍 Generator vs Normal Function

| বিষয়          | Normal Function (`return`) | Generator (`yield`)        |
| ------------- | -------------------------- | -------------------------- |
| Output system | একবারে সব রিটার্ন          | একটার পর একটা দেয়          |
| Memory Usage  | বেশি (Load everything)     | কম (Stream style)          |
| Control       | রিটার্নের পর বন্ধ          | `yield` পরে pause হয়ে থাকে |
| Example Use   | ছোট ডেটা                   | বড় ডেটা / Infinite stream  |

---

## 🚨 গুরুত্বপূর্ণ নোট: `list(generator)` করলে কী হয়?

✅ Generator আসলে **stream data giver**, কিন্তু যদি তুমি `list(generator)` করো → সব ডেটা একসাথে **memory তে লোড হবে**
❌ তখন **Generator আর memory efficient থাকবে না**

👉 তাই:

* **Memory বাঁচাতে চাইলে → `for` loop বা `next()` ব্যবহার করতে হবে**
* **List বানালে → Generator এর সুবিধা নষ্ট হবে**

---

## 🎯 Generator থেকে index দিয়ে মান access করবো কিভাবে?

➡ Generator-এ direct index নেই, কারণ ও **stream করে দেয়**
➡ তাই এইভাবে করতে হয়:

```python
for index, value in enumerate(gen_numbers()):
    if index == 5:   # 6th মান ধরে
        print(value)
        break
```

✅ **Generator + `enumerate()` = index সহ access** (মেমরি বাঁচলো)

---

## ✅ কখন কোনটা ব্যবহার করবো?

| কাজ                      | List         | Generator                       |
| ------------------------ | ------------ | ------------------------------- |
| সব ডেটা একসাথে দরকার     | ✅ List       | ❌ Not good                      |
| ডেটা একটার পর একটা দরকার | ✅ সম্ভব      | ✅ Best                          |
| বড় ডেটা / Streaming      | ❌ সমস্যা হবে | ✅ Perfect choice                |
| Random index access      | ✅ list[5]    | ⚠ enumerate method দিয়ে করতে হয় |

---

## 🎓 Final Summary (মনে রাখার মতো বাক্য)

> **Iterator = next() দিয়ে ধারাবাহিকভাবে মান নেওয়ার সিস্টেম**
> **Generator = yield দিয়ে নিজের Iterator তৈরি করা যায়, মেমরি না খেয়ে**
> **List বানালে Generator এর সুবিধা শেষ — তাই stream করে ব্যবহার করাই আসল power**

---
# 🚀 Python Iterator & Generator (সহজ ভাষায়, উদাহরণসহ)

## 1) Fibonacci Generator (Infinite / First N / K-th)

```python
def fib():
    """Infinite Fibonacci generator: 0, 1, 1, 2, 3, 5, ..."""
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b
```

### ব্যবহার:

```python
# প্রথম 10টা Fibonacci
for i, v in enumerate(fib()):
    if i == 10: break
    print(v, end=" ")      # 0 1 1 2 3 5 8 13 21 34 55

# K-তম Fibonacci (0-indexed)
def kth_fib(k):
    for i, v in enumerate(fib()):
        if i == k:
            return v

print(kth_fib(50))         # 50তম (0-indexed) Fibonacci
```

> টিপ: **list(fib()) করবেন না**—অসীম স্ট্রিম। `enumerate` + `break` ব্যবহার করাই নিরাপদ।

---

## 2) Prime Number Generator (Memory-efficient)

```python
def primes():
    """Infinite prime generator: 2, 3, 5, 7, 11, ..."""
    yield 2
    found = [2]
    n = 3
    while True:
        is_prime = True
        limit = int(n**0.5)
        for p in found:
            if p > limit: break
            if n % p == 0:
                is_prime = False
                break
        if is_prime:
            found.append(n)
            yield n
        n += 2  # even স্কিপ
```

### ব্যবহার:

```python
# প্রথম 15টা prime
for i, p in enumerate(primes()):
    if i == 15: break
    print(p, end=" ")      # 2 3 5 7 11 13 17 19 23 29 31 37 41 43 47

# K-তম prime (0-indexed)
def kth_prime(k):
    for i, p in enumerate(primes()):
        if i == k:
            return p

print(kth_prime(1000))     # 1001তম prime
```

> টিপ: এপ্রোচটা **trial-division with cached primes**—সহজ ও যথেষ্ট দ্রুত। খুব বড় রেঞ্জে চাইলে segmented sieve/optimized পদ্ধতি নিলে আরও দ্রুত হবে।

---

## 3) File Loader (লাইন/চাঙ্ক স্ট্রিমিং)

### (a) Line-by-Line Loader — বিশাল ফাইলেও RAM safe

```python
def read_lines(path, encoding="utf-8"):
    """Yield lines one by one (newline সহ/ছাড়া চাইলে rstrip করুন)।"""
    with open(path, "r", encoding=encoding) as f:
        for line in f:
            yield line  # বা yield line.rstrip("\n")
```

### ব্যবহার:

```python
for i, line in enumerate(read_lines("big.log")):
    if i == 5: break
    print(line.rstrip())
```

### (b) Chunk Loader — বড় বাইনারি/টেক্সট চাঙ্কে পড়া

```python
def read_chunks(path, chunk_size=1024 * 1024):
    """Yield fixed-size byte chunks (e.g., 1MB)."""
    with open(path, "rb") as f:
        while True:
            chunk = f.read(chunk_size)
            if not chunk:
                break
            yield chunk
```

### ব্যবহার:

```python
total = 0
for chunk in read_chunks("video.mp4", chunk_size=4*1024*1024):
    total += len(chunk)
print("Bytes read:", total)
```

### (c) CSV Row Streamer — row-by-row প্রসেসিং

```python
import csv

def read_csv_rows(path, encoding="utf-8"):
    with open(path, "r", encoding=encoding, newline="") as f:
        reader = csv.DictReader(f)
        for row in reader:
            yield row
```

### ব্যবহার:

```python
for i, row in enumerate(read_csv_rows("students.csv")):
    if i == 10: break
    print(row["name"], row["marks"])
```

> টিপস
>
> * **Generator = স্ট্রিম**: বড় ফাইল প্রসেসিংয়ে `for` লুপে প্রসেস করুন।
> * **Index দরকার?** `enumerate()` ব্যবহার করুন—list বানাবেন না।
> * I/O-heavy হলে **চাঙ্ক সাইজ** টিউন করুন (যেমন 256KB, 1MB, 4MB)।

---

## Bonus: Custom Iterator Class (বোঝাটা পাকাপোক্ত হবে)

```python
class Countdown:
    def __init__(self, start):
        self.cur = start
    def __iter__(self):
        return self
    def __next__(self):
        if self.cur < 0:
            raise StopIteration
        val = self.cur
        self.cur -= 1
        return val

for x in Countdown(5):
    print(x, end=" ")  # 5 4 3 2 1 0
```

---

### দ্রুত সারসংক্ষেপ

* **Fibonacci/Prime**: অসীম সিরিজ—`yield` দিয়ে স্ট্রিম করুন, `enumerate+break` এ থামুন।
* **File Loader**: লাইন/চাঙ্ক/CSV—সবকিছু **লেজি** লোডিং; RAM সেফ।
* **Index লাগলে**: Generator-এ direct নেই; `enumerate` বা ছোট helper (`kth_*`) ব্যবহার করুন।
* **Never**: `list(generator)`—এটা করলে memory সুবিধা নষ্ট হবে।


# 🧠 Lambda Function — একদম সহজভাবে বুঝো

**Lambda Function = একলাইনের ছোট function**, যেটা **নাম ছাড়া** (anonymous) হয়।

🔹 **সাধারণ function** 👉 `def` দিয়ে লিখি
🔹 **Lambda function** 👉 `lambda` দিয়ে লিখি (**এক লাইনে কাজ সেরে ফেলে**)

---

### 🎯 Basic Syntax

```python
lambda parameter: expression
```

👉 মানে: **প্যারামিটার নাও → এক লাইনে রেজাল্ট রিটার্ন করো**

---

### ✅ উদাহরণ ১ — Normal Function vs Lambda

#### 🟥 Normal Function:

```python
def add(a, b):
    return a + b

print(add(5, 3))
```

#### ✅ Lambda Function (Same কাজ এক লাইনে):

```python
add = lambda a, b: a + b
print(add(5, 3))
```

🔹 Output: `8`

---

### ✅ উদাহরণ ২ — Square বের করা

```python
square = lambda x: x * x
print(square(6))   # Output: 36
```

---

### ✅ উদাহরণ ৩ — Even or Odd

```python
is_even = lambda x: x % 2 == 0
print(is_even(10))  # True
print(is_even(7))   # False
```

---

### 💡 কোথায় Lambda বেশি ব্যবহার হয়?

| ব্যবহার                                 | Lambda কেন কাজে লাগে       |
| --------------------------------------- | -------------------------- |
| ছোট হিসাব করতে                          | def লিখতে হয় না            |
| এক লাইনের quick ফাংশন                   | কোড ছোট ও clean থাকে       |
| `map()`, `filter()`, `sorted()` এর সাথে | Lambda খুব জনপ্রিয় এখানে ⚡ |

---

### 🧪 Bonus Example: filter + lambda দিয়ে even number নেওয়া

```python
numbers = [1, 2, 3, 4, 5, 6]
evens = list(filter(lambda x: x % 2 == 0, numbers))
print(evens)   # Output: [2, 4, 6]
```

---

### 🎯 এক লাইনে মনে রাখো:

> **Lambda = নাম ছাড়াই ছোট function → এক লাইনে লেখা যায় → যেখানে ছোট কাজ করতে def লিখে ঝামেলা করতে চাই না।**

# 🚀 `map()` Function in Python — একদম সহজভাবে

**`map()` ব্যবহার করা হয় — একটি function কে list বা যেকোন iterable-এর প্রতিটি আইটেমের উপর apply করতে।**

👉 মানে: **"List-এর প্রতিটা মানে ফাংশন চালাও" — এই কাজটাই map করে।**

---

### 🎯 Basic Syntax:

```python
map(function, iterable)
```

* **function** → যেটা apply হবে
* **iterable** → list, tuple, etc.

---

### ✅ Example 1 — প্রতিটা সংখ্যাকে 2 দিয়ে গুণ করা

#### 🟥 Normal for loop করে

```python
numbers = [1, 2, 3, 4]
result = []
for i in numbers:
    result.append(i * 2)

print(result)  # [2, 4, 6, 8]
```

#### ✅ Same কাজ `map()` + `lambda` দিয়ে (এক লাইনে!)

```python
numbers = [1, 2, 3, 4]
result = list(map(lambda x: x * 2, numbers))
print(result)  # [2, 4, 6, 8]
```

---

### ✅ Example 2 — List-এর সব স্ট্রিং uppercase করা

```python
names = ["rahim", "karim", "lima"]
result = list(map(lambda x: x.upper(), names))
print(result)  # ['RAHIM', 'KARIM', 'LIMA']
```

---

### ✅ Example 3 — দুইটা লিস্টের মান যোগ করা

```python
a = [1, 2, 3]
b = [4, 5, 6]
result = list(map(lambda x, y: x + y, a, b))
print(result)  # [5, 7, 9]
```

---

### 🎯 Summary Table

| কাজ                   | Old Way    | Smart Way               |
| --------------------- | ---------- | ----------------------- |
| প্রতিটা item প্রোসেস  | `for` loop | ✅ `map(function, list)` |
| Function apply        | Manual     | ✅ `lambda + map`        |
| Multiple list combine | Hard       | ✅ map(lambda x, y: ...) |

---

### 🔥 এক লাইনে মনে রাখো:

> **`map()` = "List-এর প্রতিটি আইটেমের উপর ফাংশন চালাও" — এবং `lambda` থাকলে এক লাইনে whole কাজ শেষ!**

# ✅ `filter()` Function in Python — একদম সহজভাবে

**`filter()` ব্যবহার করা হয় — list বা iterable থেকে শুধু নির্দিষ্ট শর্ত পূরণ করা আইটেমগুলো বাছাই করতে।**

👉 সহজভাবে: **"কোন শর্তে সত্য হলে, সেই আইটেমটা রেখে দাও"**

---

### 🎯 Basic Syntax

```python
filter(function, iterable)
```

* **function** → শর্ত (True/False return করতে হবে)
* **iterable** → list, tuple, etc.

---

## ✅ Example 1 — শুধুমাত্র জোড় সংখ্যা রাখা

### 🟥 Normal for loop:

```python
numbers = [1, 2, 3, 4, 5, 6]
result = []
for i in numbers:
    if i % 2 == 0:
        result.append(i)

print(result)  # [2, 4, 6]
```

### ✅ Same কাজ — `filter()` + `lambda` দিয়ে:

```python
numbers = [1, 2, 3, 4, 5, 6]
result = list(filter(lambda x: x % 2 == 0, numbers))
print(result)  # [2, 4, 6]
```

---

## ✅ Example 2 — List থেকে ৫ এর বেশি মান বাদ দিয়ে ফিল্টার করা

```python
numbers = [3, 8, 1, 10, 6, 2]
result = list(filter(lambda x: x > 5, numbers))
print(result)  # [8, 10, 6]
```

---

## ✅ Example 3 — নামের লিস্ট থেকে যেগুলোর length > 4 শুধু সেগুলো রাখা

```python
names = ["Rony", "Amina", "Karim", "Bob"]
result = list(filter(lambda name: len(name) > 4, names))
print(result)  # ['Amina', 'Karim']
```

---

### 🎯 Comparison Table

| কাজ                          | Old Way (for loop) | Smart Way (filter + lambda) |
| ---------------------------- | ------------------ | --------------------------- |
| Data pick based on condition | ✅                  | ✅✅ আরও clean                |
| Extra code line লাগে?        | হ্যাঁ              | না                          |
| ফাংশনালি clean?              | ❌                  | ✅                           |

---

### 🎁 Bonus: **Even + Odd একসাথে ফিল্টার**

```python
numbers = [1, 2, 3, 4, 5, 6]

evens = list(filter(lambda x: x % 2 == 0, numbers))
odds = list(filter(lambda x: x % 2 != 0, numbers))

print("Even:", evens)
print("Odd:", odds)
```

---

### 💡 এক লাইনে মনে রাখো:

> **filter() = Condition true হলে data রাখবে, false হলে বাদ দেবে ✅**

### 🚀 `sorted()` Function in Python — একদম সহজভাবে

`sorted()` ব্যবহার করা হয় **list, tuple, dictionary, set — যেকোনো iterable কে সাজানোর জন্য**।

👉 এটা **নতুন list রিটার্ন করে**, মূল ডেটা চেঞ্জ করে না (অপরিবর্তিত থাকে) ✅

---

### 🎯 Basic Syntax:

```python
sorted(iterable, key=None, reverse=False)
```

| Parameter      | কাজ                                           |
| -------------- | --------------------------------------------- |
| `iterable`     | যেটাকে sort করতে চাই (list, tuple, etc.)      |
| `key`          | কিভাবে sort হবে — custom rule দিতে ব্যবহার হয় |
| `reverse=True` | উল্টো করে sort করতে                           |

---

## ✅ Simple Example – Normal Sorting

```python
numbers = [5, 1, 7, 3, 2]
print(sorted(numbers))
# Output: [1, 2, 3, 5, 7]
```

👉 **মূল লিস্ট চেঞ্জ হয়নি**

```python
print(numbers)  # [5, 1, 7, 3, 2]
```

---

## ✅ Sorting in Reverse Order

```python
print(sorted(numbers, reverse=True))
# Output: [7, 5, 3, 2, 1]
```

---

## 🔥 `sorted()` with `key` + `lambda` (Powerful Trick 💡)

### 🎯 Example: String list sort by **length**

```python
names = ["Rahim", "Lima", "Abdullah", "Amin"]
result = sorted(names, key=lambda x: len(x))
print(result)
# Output: ['Lima', 'Amin', 'Rahim', 'Abdullah']
```

---

### 🎯 Example: Sort Dictionary List by **marks**

```python
students = [
    {"name": "Rahim", "marks": 85},
    {"name": "Karim", "marks": 92},
    {"name": "Lima", "marks": 78}
]

sorted_students = sorted(students, key=lambda x: x['marks'], reverse=True)
print(sorted_students)
```

✅ Output:

```
[{'name': 'Karim', 'marks': 92}, {'name': 'Rahim', 'marks': 85}, {'name': 'Lima', 'marks': 78}]
```

👉 এখানে **marks এর ভিত্তিতে সাজিয়েছে, Highest first**

---

### 🎯 Summary Table

| কাজ                  | কোড                               |
| -------------------- | --------------------------------- |
| Ascending sort       | `sorted(list)`                    |
| Descending sort      | `sorted(list, reverse=True)`      |
| Custom sort          | `sorted(list, key=lambda x: ...)` |
| Dictionary list sort | `key=lambda x: x['key_name']`     |

---

### 🎁 এক লাইনে মনে রাখো:

> **sorted() = সাজানোর মেশিন + lambda দিলে কাস্টম নিয়মে সাজাতে পারো**

# 🚀 `reduce()` in Python — একদম সহজভাবে বোঝো

**`reduce()` ব্যবহার করা হয় যখন তুমি একটি তালিকা বা iterable-এর সব মানকে একত্র করে একটি final result বানাতে চাও।**

👉 মানে **"সবগুলো মানকে একসাথে মিশিয়ে একটি output তৈরি করো"**

---

### 🔧 Syntax:

```python
from functools import reduce
reduce(function, iterable)
```

* `function` → দুইটা ভ্যালু নিয়ে কাজ করে (`lambda a, b: ...`)
* `iterable` → list, tuple ইত্যাদি

---

## ✅ Example 1 — সব সংখ্যা যোগ করা (Sum without sum())

### 🟥 Normal Loop way:

```python
numbers = [1, 2, 3, 4]
total = 0
for num in numbers:
    total += num
print(total)  # Output: 10
```

### ✅ Same কাজ `reduce()` দিয়ে এক লাইনে:

```python
from functools import reduce

numbers = [1, 2, 3, 4]
result = reduce(lambda a, b: a + b, numbers)
print(result)  # Output: 10
```

---

## ✅ Example 2 — সব সংখ্যার গুণফল করা (Factorial Logic)

```python
from functools import reduce

numbers = [1, 2, 3, 4]
result = reduce(lambda a, b: a * b, numbers)
print(result)  # Output: 24
```

---

## ✅ Example 3 — লিস্ট থেকে **সর্বোচ্চ মান (max)** বের করা reduce দিয়ে

```python
from functools import reduce

numbers = [5, 12, 3, 19, 7]
result = reduce(lambda a, b: a if a > b else b, numbers)
print(result)  # Output: 19
```

---

## 🎯 reduce() কোথায় কাজে লাগে?

| প্রয়োজন        | Built-in নেই?          | reduce কাজে লাগবে? |
| -------------- | ---------------------- | ------------------ |
| Sum            | ✅ আছে → `sum()`        | ❌ দরকার নেই        |
| Max/Min        | ✅ আছে → `max(), min()` | ❌ দরকার নেই        |
| Custom Combine | ❌ নিজে তৈরি করতে হবে   | ✅ reduce perfect!  |

👉 তাই **reduce() = যখন built-in নেই কিন্তু সব ডেটা জোড়া লাগিয়ে final result দরকার।**

---

### 🎁 এক লাইনে মনে রাখো:

> **reduce() = list-এর সব মান একত্রে **“কম্প্রেস”** করে একটি single output বানাও।**

