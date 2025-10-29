# 🧠 Matplotlib কী?

**Matplotlib** হলো Python-এর একটি জনপ্রিয় library, যা দিয়ে তুমি ডেটা ভিজুয়ালাইজ করতে পারো (মানে, ডেটাকে চার্ট বা গ্রাফ আকারে দেখাতে পারো)।
সবচেয়ে বেশি ব্যবহৃত অংশ হলো:

```python
import matplotlib.pyplot as plt
```

`pyplot` হলো Matplotlib-এর এমন একটি মডিউল যা গ্রাফ আঁকা সহজ করে দেয়।

---

## 📊 Matplotlib দিয়ে সাধারণ উদাহরণ

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 35]

plt.plot(x, y)
plt.title("Simple Line Graph")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

এটা একটি **Line Graph** তৈরি করবে।

---

## 📈 Matplotlib-এ ব্যবহৃত জনপ্রিয় গ্রাফগুলো

### 1️⃣ **Line Graph**

📍 **ব্যবহার:** সময়ের সাথে সাথে পরিবর্তন দেখাতে।
উদাহরণ: কোনো কোম্পানির বছরের প্রতি মাসে বিক্রি কত হলো।

```python
plt.plot(x, y)
```

---

### 2️⃣ **Bar Chart**

📍 **ব্যবহার:** বিভিন্ন ক্যাটাগরির তুলনা করতে।
উদাহরণ: তিনটি প্রোডাক্টের সেলস তুলনা।

```python
categories = ['A', 'B', 'C']
values = [100, 250, 150]

plt.bar(categories, values)
```

---

### 3️⃣ **Histogram**

📍 **ব্যবহার:** ডেটার distribution (বন্টন) বোঝার জন্য।
উদাহরণ: ছাত্রদের মার্কস কীভাবে ছড়ানো আছে।

```python
marks = [45, 56, 67, 67, 70, 75, 80, 82, 85, 90]
plt.hist(marks, bins=5)
```

---

### 4️⃣ **Scatter Plot**

📍 **ব্যবহার:** দুইটা ভেরিয়েবলের মধ্যে সম্পর্ক (correlation) বোঝার জন্য।
উদাহরণ: height vs weight।

```python
height = [150, 160, 170, 180, 190]
weight = [50, 60, 70, 80, 90]
plt.scatter(height, weight)
```

---

### 5️⃣ **Pie Chart**

📍 **ব্যবহার:** কোনো কিছুর শতকরা ভাগ বোঝাতে।
উদাহরণ: মার্কেট শেয়ার বা বাজেট ভাগ।

```python
labels = ['Rent', 'Food', 'Bills', 'Others']
sizes = [40, 30, 20, 10]
plt.pie(sizes, labels=labels, autopct='%1.1f%%')
```

---

### 6️⃣ **Box Plot**

📍 **ব্যবহার:** ডেটার distribution ও outlier বোঝাতে।
উদাহরণ: পরীক্ষার রেজাল্টে কোনো outlier আছে কিনা।

```python
data = [25, 30, 35, 40, 45, 50, 100]
plt.boxplot(data)
```

---

## 🧭 কখন কোন গ্রাফ ব্যবহার করবে?

| উদ্দেশ্য                     | উপযুক্ত গ্রাফ        |
| ---------------------------- | -------------------- |
| সময়ের সাথে পরিবর্তন          | Line Chart           |
| বিভিন্ন ক্যাটাগরির তুলনা     | Bar Chart            |
| ডেটার বন্টন দেখতে            | Histogram / Box Plot |
| দুই ভেরিয়েবলের সম্পর্ক দেখতে | Scatter Plot         |
| শতাংশ বা ভাগ দেখাতে          | Pie Chart            |

---

## ⚙️ Matplotlib ইনস্টল করা

তুমি যদি Python ইনস্টল করে থাকো, তাহলে Matplotlib ইনস্টল করতে শুধু একটা কমান্ড চালালেই হবে:

```bash
pip install matplotlib
```

✅ ইনস্টল শেষ হলে নিচের কোড চালিয়ে যাচাই করতে পারো:

```python
import matplotlib
print(matplotlib.__version__)
```

যদি কোনো এরর না আসে, তাহলে বুঝবে Matplotlib ঠিকভাবে ইনস্টল হয়েছে।

---

## 🧩 Matplotlib-এর মূল অংশ: pyplot

Matplotlib-এ সবচেয়ে বেশি ব্যবহৃত মডিউল হলো **`pyplot`**
এটা দিয়ে গ্রাফ আঁকা একদম সহজ হয়।

```python
import matplotlib.pyplot as plt
```

এখানে `plt` হলো একটি শর্ট নাম (alias) — যাতে কম লিখে কাজ করা যায়।

---

## 🧮 প্রথম গ্রাফ 🎨

- Line Graph বানাই 👇

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]   # X-axis data
y = [10, 20, 25, 30, 35]  # Y-axis data

plt.plot(x, y)           # লাইন আঁকা
plt.title("My First Graph")  # শিরোনাম
plt.xlabel("X-Axis")     # X অক্ষের লেবেল
plt.ylabel("Y-Axis")     # Y অক্ষের লেবেল
plt.show()               # গ্রাফ দেখানো
```

🔹 `plt.plot()` → লাইন গ্রাফ আঁকে
🔹 `plt.title()`, `plt.xlabel()`, `plt.ylabel()` → টাইটেল ও লেবেল দেয়
🔹 `plt.show()` → গ্রাফ দেখায়

---

## 🎨 আউটপুট

এই কোড চালালে একটি **সোজা লাইন গ্রাফ** দেখা যাবে যেখানে X মান বাড়লে Y মানও বাড়ছে।
অর্থাৎ, এটি সময় বা পরিবর্তনের সাথে বৃদ্ধির একটি ট্রেন্ড দেখায়।

---

## 📚 আজকের সারসংক্ষেপ

| বিষয়               | বর্ণনা                                |
| ------------------ | ------------------------------------- |
| Matplotlib কী      | Python library for data visualization |
| কিভাবে ইনস্টল করবে | `pip install matplotlib`              |
| প্রধান মডিউল       | `pyplot`                              |
| প্রথম কোড          | `plt.plot(x, y)` + `plt.show()`       |

---

চমৎকার! 🎯
তাহলে চল আজকের পাঠ শুরু করি —

# 🧩 **Line Graph বিস্তারিতভাবে **

---

## 📈 ১. Line Graph কী?

**Line Graph** (বা Line Chart) হলো এমন এক ধরণের গ্রাফ যেখানে ডেটা পয়েন্টগুলোকে লাইন দিয়ে যুক্ত করা হয়।
এটা দিয়ে সাধারণত **সময় অনুযায়ী পরিবর্তন** (trend) দেখানো হয়।

📊 উদাহরণ:

- একটি কোম্পানির ৬ মাসের বিক্রি
- একজন ছাত্রের প্রতিদিনের পড়ার সময়
- কোনো শহরের তাপমাত্রা পরিবর্তন

---

## 🧮 ২. একটি সাধারণ Line Graph

চলো একটা সহজ উদাহরণ দেখি 👇

```python
import matplotlib.pyplot as plt

# ডেটা
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
sales = [100, 120, 140, 160, 180, 200]

# গ্রাফ আঁকা
plt.plot(months, sales)

# লেবেল ও শিরোনাম
plt.title("Monthly Sales Report")
plt.xlabel("Months")
plt.ylabel("Sales (in Units)")

# গ্রাফ দেখানো
plt.show()
```

🔹 এখানে প্রতিটি মাসের বিক্রি লাইন দিয়ে যুক্ত হয়েছে, যা সময়ের সাথে বৃদ্ধির ট্রেন্ড দেখাচ্ছে।

---

## 🎨 ৩. লাইন রঙ, স্টাইল ও মার্কার পরিবর্তন

তুমি চাইলে লাইনকে আরো সুন্দর করে কাস্টমাইজ করতে পারো।

```python
plt.plot(months, sales, color='green', linestyle='--', marker='o')
```

👉 ব্যাখ্যা:

- `color='green'` → লাইন সবুজ হবে
- `linestyle='--'` → ড্যাশড লাইন হবে
- `marker='o'` → প্রতিটি পয়েন্টে গোল চিহ্ন দেখাবে

🔹 কিছু সাধারণ marker:

| Marker | মানে     |
| ------ | -------- |
| `o`    | Circle   |
| `s`    | Square   |
| `^`    | Triangle |
| `*`    | Star     |

🔹 কিছু সাধারণ linestyle:

| Style  | মানে          |
| ------ | ------------- |
| `'-'`  | Solid line    |
| `'--'` | Dashed line   |
| `'-.'` | Dash-dot line |
| `':'`  | Dotted line   |

---

## 🧠 ৪. একাধিক লাইন একসাথে আঁকা

একই গ্রাফে একাধিক লাইন আঁকা যায় — তুলনা করার জন্য দারুণ কাজে লাগে।

```python
months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
sales_A = [100, 120, 140, 160, 180, 200]
sales_B = [90, 110, 130, 150, 170, 190]

plt.plot(months, sales_A, color='blue', marker='o', label='Product A')
plt.plot(months, sales_B, color='red', marker='s', label='Product B')

plt.title("Sales Comparison")
plt.xlabel("Months")
plt.ylabel("Sales (in Units)")

plt.legend()  # এটি লাইনগুলোর নাম দেখাবে
plt.show()
```

👉 এখানে আমরা `plt.legend()` ব্যবহার করেছি যাতে লাইনগুলোর নাম (label) দেখা যায়।

---

## 🖼️ ৫. লাইন থিকনেস ও Figure Size

তুমি লাইন কতটা মোটা বা চিকন হবে, সেটাও নির্ধারণ করতে পারো।

```python
plt.plot(months, sales, color='purple', linewidth=3)
```

এছাড়া পুরো ছবির আকার (figure size) বদলানো যায়:

```python
plt.figure(figsize=(8,5))
plt.plot(months, sales)
plt.show()
```

---

## 📋 ৬. সারসংক্ষেপ (আজ যা শিখলে)

| বিষয়             | কমান্ড                                      | ব্যাখ্যা               |
| ---------------- | ------------------------------------------- | ---------------------- |
| বেসিক লাইন গ্রাফ | `plt.plot(x, y)`                            | সাধারণ লাইন গ্রাফ আঁকা |
| রঙ পরিবর্তন      | `color='red'`                               | লাইন রঙ                |
| স্টাইল পরিবর্তন  | `linestyle='--'`                            | ড্যাশড / ডটেড          |
| মার্কার যোগ      | `marker='o'`                                | পয়েন্টে চিহ্ন          |
| একাধিক লাইন      | `plt.plot(..., label='A')` + `plt.legend()` | তুলনামূলক চার্ট        |
| Figure Size      | `plt.figure(figsize=(8,5))`                 | ছবির আকার              |

---

দারুণ! 🚀
আজ আমরা শিখব —

# 🎯 Bar Chart ও Histogram

---

## 📊 ১. Bar Chart কী?

**Bar Chart** হলো এমন এক ধরণের গ্রাফ যেখানে বিভিন্ন **ক্যাটাগরি বা গ্রুপের মানকে বার (আয়তক্ষেত্র)** আকারে দেখানো হয়।
এটা তুলনামূলক বিশ্লেষণের জন্য দারুণ উপযোগী।

📍 **ব্যবহার:**

- বিভিন্ন প্রোডাক্টের বিক্রি তুলনা
- ক্লাসের ছাত্রদের মার্কস তুলনা
- বছরের বিভিন্ন মাসের আয় ব্যয়

---

## 🧮 ২. একটি সাধারণ Bar Chart

```python
import matplotlib.pyplot as plt

# ডেটা
products = ['A', 'B', 'C', 'D']
sales = [150, 200, 300, 250]

# বার চার্ট আঁকা
plt.bar(products, sales)

# লেবেল ও শিরোনাম
plt.title("Product Sales Comparison")
plt.xlabel("Products")
plt.ylabel("Sales (in Units)")

plt.show()
```

📈 প্রতিটি প্রোডাক্টের জন্য একটি বার তৈরি হবে — যার উচ্চতা সেই প্রোডাক্টের বিক্রির মান বোঝাবে।

---

## 🎨 ৩. রঙ, প্রস্থ ও বর্ডার পরিবর্তন

তুমি বারগুলো কাস্টমাইজ করতে পারো:

```python
plt.bar(products, sales, color='skyblue', width=0.6, edgecolor='black')
```

- `color` → বারগুলোর রঙ
- `width` → বার কতটা মোটা বা চিকন হবে
- `edgecolor` → বর্ডারের রঙ

---

## ↔️ ৪. Horizontal Bar Chart

যদি তুমি চাও বারগুলো অনুভূমিকভাবে দেখাতে:

```python
plt.barh(products, sales, color='orange')
plt.title("Product Sales (Horizontal Bar)")
plt.xlabel("Sales (in Units)")
plt.ylabel("Products")
plt.show()
```

এখানে `barh()` ব্যবহার করা হয়েছে — h মানে “horizontal”।

---

## 📊 ৫. একাধিক Bar তুলনা (Side by Side)

দুটি প্রোডাক্ট লাইন তুলনা করতে পারো এভাবে 👇

```python
import numpy as np

products = ['A', 'B', 'C', 'D']
sales_2024 = [150, 200, 300, 250]
sales_2025 = [180, 220, 310, 270]

x = np.arange(len(products))  # অবস্থান নির্ধারণ
width = 0.35

plt.bar(x - width/2, sales_2024, width, label='2024', color='blue')
plt.bar(x + width/2, sales_2025, width, label='2025', color='green')

plt.xlabel('Products')
plt.ylabel('Sales')
plt.title('Sales Comparison (2024 vs 2025)')
plt.xticks(x, products)
plt.legend()
plt.show()
```

এতে তুমি পাশাপাশি দুই বছরের তুলনামূলক গ্রাফ দেখতে পাবে।

---

## 📦 ৬. Histogram কী?

**Histogram** হলো এমন এক ধরণের গ্রাফ যা দেখায় **কোন মান কতবার ঘটছে (frequency)**।
এটা মূলত **continuous data** (যেমন বয়স, মার্কস, সময় ইত্যাদি)-এর distribution বোঝাতে ব্যবহৃত হয়।

📍 **ব্যবহার:**

- ছাত্রদের মার্কসের বণ্টন
- মানুষের বয়সের গ্রুপ অনুযায়ী সংখ্যা
- ডেটার variation বা spread বোঝা

---

## 🧮 ৭. Histogram উদাহরণ

```python
import matplotlib.pyplot as plt

marks = [40, 42, 45, 50, 52, 55, 60, 62, 63, 65, 67, 70, 72, 75, 80, 85, 90]

plt.hist(marks, bins=5, color='lightgreen', edgecolor='black')
plt.title("Students Marks Distribution")
plt.xlabel("Marks Range")
plt.ylabel("Number of Students")
plt.show()
```

📊 এখানে `bins=5` মানে — পুরো রেঞ্জকে ৫টা ভাগে ভাগ করা হয়েছে (যেমন 40–50, 50–60 ইত্যাদি)।

---

## 🔍 ৮. Bar Chart vs Histogram পার্থক্য

| বিষয়      | Bar Chart               | Histogram              |
| --------- | ----------------------- | ---------------------- |
| ডেটা টাইপ | ক্যাটাগরি (Discrete)    | ধারাবাহিক (Continuous) |
| ব্যবধান   | বারগুলোর মাঝে ফাঁক থাকে | কোনো ফাঁক থাকে না      |
| ব্যবহার   | তুলনা দেখাতে            | distribution দেখাতে    |

---

দারুণ! 😄
তাহলে আমরা এখন শুরু করছি —

# 🎯 Scatter Plot

---

## 🔵 ১. Scatter Plot কী?

**Scatter Plot** হলো এমন এক ধরণের গ্রাফ যেখানে দুইটি ভেরিয়েবলের (variables) মধ্যে **সম্পর্ক বা correlation** দেখানো হয়।
প্রতিটি ডেটা পয়েন্ট একটি **(x, y)** coordinate আকারে প্লট হয়।

📍 **ব্যবহার:**

- মানুষের উচ্চতা বনাম ওজন
- তাপমাত্রা বনাম আইসক্রিম বিক্রি
- পড়ার সময় বনাম পরীক্ষার নম্বর

---

## 🧮 ২. একটি সাধারণ Scatter Plot

```python
import matplotlib.pyplot as plt

height = [150, 155, 160, 165, 170, 175, 180]
weight = [50, 55, 60, 65, 70, 75, 80]

plt.scatter(height, weight)
plt.title("Height vs Weight")
plt.xlabel("Height (cm)")
plt.ylabel("Weight (kg)")
plt.show()
```

📊 এখানে প্রতিটি ডট একজন ব্যক্তির height ও weight নির্দেশ করছে।

---

## 🎨 ৩. রঙ, আকার ও marker পরিবর্তন

তুমি scatter plot-কে সুন্দরভাবে customize করতে পারো:

```python
plt.scatter(height, weight, color='green', marker='o', s=100, edgecolor='black')
```

- `color='green'` → ডট সবুজ হবে
- `marker='o'` → গোল মার্কার
- `s=100` → মার্কারের সাইজ
- `edgecolor='black'` → কালো বর্ডার

🔹 কিছু সাধারণ marker:

| Marker | মানে     |
| ------ | -------- |
| `o`    | Circle   |
| `s`    | Square   |
| `^`    | Triangle |
| `*`    | Star     |
| `x`    | Cross    |

---

## 📈 ৪. একাধিক Scatter একসাথে

যদি তুমি দুইটা ভিন্ন গ্রুপ বা সেটের ডেটা এক গ্রাফে দেখাতে চাও:

```python
x1 = [1, 2, 3, 4, 5]
y1 = [2, 4, 6, 8, 10]

x2 = [1, 2, 3, 4, 5]
y2 = [1, 3, 5, 7, 9]

plt.scatter(x1, y1, color='blue', label='Group A')
plt.scatter(x2, y2, color='red', label='Group B')

plt.title("Multiple Scatter Example")
plt.xlabel("X values")
plt.ylabel("Y values")
plt.legend()
plt.show()
```

🔸 `plt.legend()` → দুই গ্রুপের নাম দেখানোর জন্য।

---

## 📊 ৫. Marker Size দিয়ে Data বোঝানো (Bubble Chart)

Scatter Plot-এ তৃতীয় ভেরিয়েবল দেখাতে **marker size (s)** ব্যবহার করা হয়। একে **Bubble Chart** বলা হয়।

```python
x = [10, 20, 30, 40, 50]
y = [5, 25, 15, 35, 30]
size = [100, 200, 300, 400, 500]

plt.scatter(x, y, s=size, color='skyblue', alpha=0.6, edgecolor='black')
plt.title("Bubble Chart Example")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

- `s=size` → marker-এর আকার ভিন্ন ভিন্ন
- `alpha=0.6` → transparency

এতে বোঝানো হয় — যত বড় বাবল, তত বেশি মান।

---

## 📋 ৬. আজ যা শিখলে

| বিষয়             | ব্যাখ্যা                               |
| ---------------- | -------------------------------------- |
| Scatter Plot কী  | দুই ভেরিয়েবলের সম্পর্ক বোঝায়           |
| রঙ, আকার, marker | `color`, `s`, `marker`                 |
| একাধিক Scatter   | `plt.scatter()` একাধিকবার              |
| Bubble Chart     | Marker size দিয়ে তৃতীয় ভেরিয়েবল দেখানো |

---

চমৎকার! 🥧
তাহলে শুরু করা যাক —

# 🎯 Pie Chart

---

## 🧠 ১. Pie Chart কী?

**Pie Chart** হলো এমন একটি গ্রাফ যেখানে একটি সম্পূর্ণ জিনিসকে **বিভিন্ন অংশের শতকরা ভাগে ভাগ করে দেখানো হয়।**
এটি দেখতে অনেকটা গোল পায়েসের মতো 🍰, যেখানে প্রতিটি টুকরা (slice) একটি ক্যাটাগরির প্রতিনিধিত্ব করে।

📍 **ব্যবহার:**

- বাজেটের বিভিন্ন খাতে খরচের ভাগ
- মার্কেট শেয়ার
- সময় বা রিসোর্স বন্টন

---

## 🧮 ২. একটি সাধারণ Pie Chart

```python
import matplotlib.pyplot as plt

# ডেটা
expenses = [4000, 2500, 1500, 2000]
categories = ['Rent', 'Food', 'Bills', 'Others']

# পাই চার্ট আঁকা
plt.pie(expenses, labels=categories)

plt.title("Monthly Expenses")
plt.show()
```

🎨 এটি একটি সাধারণ Pie Chart তৈরি করবে, যেখানে প্রতিটি slice খরচের পরিমাণ অনুযায়ী বড় বা ছোট হবে।

---

## 💯 ৩. শতাংশ দেখানো (autopct)

Pie Chart-এ প্রতিটি অংশ কত শতাংশ তা দেখাতে পারো:

```python
plt.pie(expenses, labels=categories, autopct='%1.1f%%')
```

🔹 এখানে `%1.1f%%` মানে:

- `1.1f` → এক দশমিক পর্যন্ত দেখাবে
- `%%` → শতাংশ চিহ্ন

👉 আউটপুটে যেমন দেখা যাবে: `25.0%`, `37.5%` ইত্যাদি।

---

## 🎨 ৪. রঙ ও Shadow যোগ করা

তুমি চাইলে প্রতিটি slice-এর আলাদা রঙ ও হালকা ছায়া দিতে পারো 👇

```python
colors = ['gold', 'lightgreen', 'lightcoral', 'lightskyblue']

plt.pie(expenses, labels=categories, colors=colors, autopct='%1.1f%%', shadow=True)
plt.title("Monthly Expenses with Colors")
plt.show()
```

---

## 💥 ৫. Explode ইফেক্ট (এক অংশ আলাদা করা)

ধরা যাক তুমি কোনো অংশকে আলাদা করে দেখাতে চাও (যেমন সবচেয়ে বড় খরচ):

```python
explode = [0.1, 0, 0, 0]  # Rent অংশ একটু আলাদা

plt.pie(expenses, labels=categories, autopct='%1.1f%%', explode=explode, shadow=True)
plt.title("Highlighting Rent Expense")
plt.show()
```

👉 `explode` মানে হলো প্রতিটি slice কতটা দূরে থাকবে কেন্দ্র থেকে।
এখানে `0.1` মানে Rent অংশ 10% দূরে থাকবে।

---

## 🔁 ৬. Start Angle ও Orientation

Pie Chart কোন দিক থেকে শুরু হবে, সেটা তুমি ঠিক করতে পারো:

```python
plt.pie(expenses, labels=categories, autopct='%1.1f%%', startangle=90)
```

👉 এখানে `startangle=90` মানে গ্রাফ 90° থেকে শুরু হবে (উপর থেকে)।

---

## 🧩 ৭. লেজেন্ড (Legend) যোগ করা

কখনো অনেক ক্যাটাগরি থাকলে লেবেল ছোট হয়ে যায়, তখন লেজেন্ড ব্যবহার করো:

```python
plt.pie(expenses, autopct='%1.1f%%', startangle=90)
plt.legend(categories, loc="best")
plt.show()
```

---

## 📋 ৮. সারসংক্ষেপ (আজ যা শিখলে)

| বিষয়           | কমান্ড                           | কাজ                 |
| -------------- | -------------------------------- | ------------------- |
| Pie Chart তৈরি | `plt.pie(values, labels=labels)` | মৌলিক চার্ট         |
| শতাংশ দেখানো   | `autopct='%1.1f%%'`              | শতকরা ভাগ দেখায়     |
| রঙ ও shadow    | `colors`, `shadow=True`          | সৌন্দর্য বাড়ায়      |
| Explode        | `explode=[...]`                  | অংশ আলাদা করে দেখায় |
| Start Angle    | `startangle=90`                  | ঘূর্ণন নির্ধারণ     |
| Legend         | `plt.legend()`                   | লেবেল আলাদা দেখায়   |

চমৎকার! 🎯
আজ আমরা শিখব —

# 🧩 Box Plot ও Violin Plot

---

## 🎁 ১. Box Plot কী?

**Box Plot** (বা **Box-and-Whisker Plot**) হলো এমন এক ধরণের গ্রাফ যা কোনো ডেটাসেটের **distribution, median, quartiles এবং outliers** দেখায়।

এটা দিয়ে সহজে বোঝা যায় —

- ডেটার **range** (ছোট থেকে বড় মান পর্যন্ত)
- ডেটার **median (মধ্য মান)**
- ডেটা কতটা ছড়ানো বা ঘন

📍 **ব্যবহার:**

- পরীক্ষার ফলাফলে outlier আছে কি না
- কোম্পানির বেতন বণ্টন বোঝা
- মেশিন লার্নিং ডেটা বিশ্লেষণ

---

## 📊 ২. একটি সাধারণ Box Plot

```python
import matplotlib.pyplot as plt

data = [25, 30, 35, 40, 45, 50, 55, 60, 65, 100]  # 100 হলো এক outlier

plt.boxplot(data)
plt.title("Example Box Plot")
plt.ylabel("Values")
plt.show()
```

📈 এই গ্রাফে তুমি দেখবে —

- মাঝের **box** → ডেটার 50% মান কোথায় পড়ছে
- মাঝের **line** → median (মধ্য মান)
- **dots / circles** → outlier মান

---

## 📦 ৩. একাধিক ডেটাসেট তুলনা

```python
A = [20, 25, 30, 35, 40, 45, 50, 55]
B = [30, 35, 40, 45, 50, 55, 60, 70]
C = [10, 15, 20, 25, 30, 40, 50, 60]

plt.boxplot([A, B, C], labels=['Set A', 'Set B', 'Set C'])
plt.title("Multiple Data Comparison")
plt.ylabel("Values")
plt.show()
```

এতে একসাথে তিনটি ডেটাসেটের distribution তুলনা করা যাবে।

---

## 🎨 ৪. Box Plot Customize করা

তুমি box-এর রঙ, notch, ইত্যাদি পরিবর্তন করতে পারো 👇

```python
plt.boxplot(data, notch=True, patch_artist=True,
            boxprops=dict(facecolor='lightblue', color='navy'),
            medianprops=dict(color='red'))
plt.title("Customized Box Plot")
plt.show()
```

- `notch=True` → median-এর চারপাশে খাঁজ যোগ করে
- `patch_artist=True` → box-কে রঙিন করতে দেয়
- `boxprops` → বক্সের রঙ
- `medianprops` → median লাইন-এর রঙ

---

## 🎻 ৫. Violin Plot কী?

**Violin Plot** হলো Box Plot-এর আরও বিস্তারিত সংস্করণ, যা **ডেটার distribution shape** (কোন মানে বেশি ডেটা আছে) দেখায়।

📍 এটি Box Plot + Density Plot-এর সংমিশ্রণ।

---

## 🎼 ৬. Violin Plot উদাহরণ

```python
import matplotlib.pyplot as plt

data1 = [30, 35, 40, 45, 50, 55, 60, 65]
data2 = [25, 30, 35, 40, 45, 55, 70, 80]

plt.violinplot([data1, data2])
plt.title("Violin Plot Example")
plt.xlabel("Dataset")
plt.ylabel("Values")
plt.show()
```

🎻 প্রতিটি “violin” অংশ ডেটার ঘনত্ব বোঝায়:

- যত মোটা অংশ, সেখানে তত বেশি ডেটা
- মাঝের লাইন হলো median

---

## 🔍 ৭. Box Plot vs Violin Plot পার্থক্য

| বিষয়          | Box Plot                            | Violin Plot                          |
| ------------- | ----------------------------------- | ------------------------------------ |
| কাজ           | ডেটার median, range ও outlier দেখায় | ডেটার পূর্ণ distribution shape দেখায় |
| সহজে বোঝা     | তুলনামূলকভাবে সহজ                   | একটু বেশি বিস্তারিত                  |
| ব্যবহারের সময় | সাধারণ পরিসংখ্যান বিশ্লেষণে         | ডেটা distribution দেখতে              |

দারুণ! 🎨
আজ আমরা শিখব —

# 🧩 Graph Customize ও Subplot

---

## 🎯 ১. কেন গ্রাফ Customize করতে হয়?

ডেটা বোঝার জন্য শুধু গ্রাফ বানানোই যথেষ্ট নয় —
তাকে **দেখতে সুন্দর ও তথ্যবহুল** করাটাও জরুরি।
Customization মানে হলো:

- রঙ, স্টাইল ও marker পরিবর্তন
- title, label, grid, legend যোগ করা
- একসাথে একাধিক গ্রাফ (subplot) বানানো

---

## 🖋️ ২. Title, Label ও Grid যোগ করা

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 25, 30, 40]

plt.plot(x, y, color='green', marker='o')
plt.title("Sales Growth Over Time", fontsize=14)
plt.xlabel("Months", fontsize=12)
plt.ylabel("Sales (in Units)", fontsize=12)
plt.grid(True)  # grid লাইন দেখাবে
plt.show()
```

📍 **গুরুত্বপূর্ণ ফাংশনগুলো**

| ফাংশন                          | কাজ                       |
| ------------------------------ | ------------------------- |
| `plt.title()`                  | গ্রাফের শিরোনাম           |
| `plt.xlabel()`, `plt.ylabel()` | অক্ষের নাম                |
| `plt.grid(True)`               | ব্যাকগ্রাউন্ডে গ্রিড লাইন |
| `fontsize`                     | লেখার সাইজ নির্ধারণ       |

---

## 🎨 ৩. Line Style, Marker ও Color একসাথে সেট করা

```python
plt.plot(x, y, color='red', linestyle='--', marker='^', linewidth=2)
```

🔹 ব্যাখ্যা:

- `color='red'` → লাইন লাল
- `linestyle='--'` → ড্যাশড লাইন
- `marker='^'` → ত্রিভুজ চিহ্ন
- `linewidth=2` → লাইন একটু মোটা

---

## 🧭 ৪. Legend ও Background Style

```python
plt.plot(x, y, label="Product A", color='orange', marker='o')
plt.title("Product Sales")
plt.xlabel("Time")
plt.ylabel("Sales")
plt.legend(loc='lower right')  # Legend অবস্থান
plt.style.use('seaborn-v0_8-darkgrid')  # সুন্দর background
plt.show()
```

📍 `plt.legend()` লাইন বা ডেটাসেটের নাম দেখায়।
📍 `plt.style.use()` ব্যবহার করে Matplotlib-এর built-in থিম সেট করা যায়।

✅ জনপ্রিয় কিছু স্টাইল:

- `'seaborn-v0_8-darkgrid'`
- `'ggplot'`
- `'classic'`
- `'bmh'`
- `'dark_background'`

---

## 🖼️ ৫. এক উইন্ডোতে একাধিক গ্রাফ (Subplot)

তুমি চাইলে একই figure-এ একাধিক গ্রাফ রাখতে পারো।
👉 এর জন্য ব্যবহার করা হয় `plt.subplot()`।

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
y2 = [5, 10, 15, 10, 5]

# Figure তৈরি
plt.figure(figsize=(10,5))

# প্রথম গ্রাফ (1 row, 2 column, 1st position)
plt.subplot(1, 2, 1)
plt.plot(x, y1, color='blue', marker='o')
plt.title("Line Graph")

# দ্বিতীয় গ্রাফ (1 row, 2 column, 2nd position)
plt.subplot(1, 2, 2)
plt.bar(x, y2, color='green')
plt.title("Bar Chart")

plt.tight_layout()  # overlap এড়াতে
plt.show()
```

📊 এখানে:

- `subplot(1, 2, 1)` → ১টি row, ২টি column, ১ম গ্রাফ
- `subplot(1, 2, 2)` → দ্বিতীয় গ্রাফ
- `tight_layout()` → ফাঁকা জায়গা সুন্দরভাবে সাজায়

---

## 🖼️ ৬. Figure Customization

তুমি পুরো figure-এর আকার ও রঙ নিয়ন্ত্রণ করতে পারো 👇

```python
plt.figure(figsize=(8,5), facecolor='lightyellow')
plt.plot(x, y, color='purple', marker='o')
plt.title("Custom Figure Background")
plt.show()
```

📍 `facecolor` → ব্যাকগ্রাউন্ডের রঙ

দারুণ! 📊
আজ আমরা শিখব —

# 🧩 CSV / Excel Data Visualization

---

## 🎯 ১. কেন CSV বা Excel ফাইল থেকে ডেটা visualization দরকার?

বাস্তব জীবনে বেশিরভাগ ডেটা — যেমন বিক্রির রিপোর্ট, ছাত্রদের ফলাফল, স্টক প্রাইস — সবই থাকে **CSV বা Excel ফাইল** আকারে।
তাই ডেটা বিশ্লেষণের জন্য আগে সেটি **Python-এ পড়তে (read)** হয়, তারপর **Matplotlib দিয়ে visualize** করতে হয়।

---

## ⚙️ ২. আগে যা দরকার

তোমার কম্পিউটারে এই লাইব্রেরিগুলো ইনস্টল থাকতে হবে 👇

```bash
pip install pandas matplotlib openpyxl
```

- **pandas** → CSV বা Excel ফাইল পড়ার জন্য
- **matplotlib** → গ্রাফ আঁকার জন্য
- **openpyxl** → Excel (.xlsx) ফাইল পড়তে সাহায্য করে

---

## 🧮 ৩. CSV ফাইল থেকে ডেটা পড়া ও গ্রাফ বানানো

ধরা যাক, তোমার কাছে `sales.csv` নামে একটা ফাইল আছে:

📄 **sales.csv**

```
Month,Sales
Jan,200
Feb,250
Mar,300
Apr,280
May,350
Jun,400
```

👉 এখন এটা Python-এ পড়া ও visualize করা যাক:

```python
import pandas as pd
import matplotlib.pyplot as plt

# CSV ফাইল পড়া
data = pd.read_csv("sales.csv")

# ডেটা দেখা
print(data)

# লাইন চার্ট বানানো
plt.plot(data["Month"], data["Sales"], color='blue', marker='o')
plt.title("Monthly Sales Report")
plt.xlabel("Month")
plt.ylabel("Sales (in Units)")
plt.grid(True)
plt.show()
```

📊 এই কোড চালালে তুমি একটি সুন্দর **Line Graph** পাবে — যেখানে মাস অনুযায়ী বিক্রি বাড়ছে।

---

## 📘 ৪. Excel ফাইল (.xlsx) থেকে ডেটা পড়া

যদি তোমার ফাইল হয় `sales_data.xlsx`, তাহলে পড়বে এভাবে 👇

```python
import pandas as pd
import matplotlib.pyplot as plt

# Excel ফাইল পড়া
data = pd.read_excel("sales_data.xlsx")

# Bar Chart
plt.bar(data["Month"], data["Sales"], color='orange')
plt.title("Sales Data from Excel")
plt.xlabel("Month")
plt.ylabel("Sales (in Units)")
plt.show()
```

---

## 📊 ৫. একাধিক কলাম নিয়ে তুলনামূলক গ্রাফ

ধরা যাক তোমার ফাইলে দুইটি প্রোডাক্ট আছে 👇

📄 **products.csv**

```
Month,Product_A,Product_B
Jan,200,150
Feb,250,180
Mar,300,220
Apr,280,260
May,350,310
Jun,400,370
```

👉 এখন তুলনামূলক লাইন গ্রাফ বানানো যাক:

```python
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("products.csv")

plt.plot(data["Month"], data["Product_A"], label="Product A", marker='o')
plt.plot(data["Month"], data["Product_B"], label="Product B", marker='s')

plt.title("Product A vs Product B Sales")
plt.xlabel("Month")
plt.ylabel("Sales (in Units)")
plt.legend()
plt.grid(True)
plt.show()
```

🔹 এখানে `plt.legend()` দিয়ে দুই প্রোডাক্টের নাম দেখানো হয়েছে।

---

## 🧩 ৬. Pie Chart বানানো (CSV থেকে)

যদি CSV-তে কোনো ক্যাটাগরি অনুযায়ী মান থাকে, তাহলে Pie Chart বানানো যাবে 👇

📄 **expenses.csv**

```
Category,Amount
Rent,4000
Food,2500
Bills,1500
Others,2000
```

```python
import pandas as pd
import matplotlib.pyplot as plt

data = pd.read_csv("expenses.csv")

plt.pie(data["Amount"], labels=data["Category"], autopct='%1.1f%%', startangle=90)
plt.title("Monthly Expense Distribution")
plt.show()
```

🥧 এতে প্রতিটি ক্যাটাগরির খরচ শতকরা ভাগে দেখা যাবে।

---

## 💡 ৭. CSV থেকে Filter করে Plot করা

তুমি চাইলে শর্ত দিয়ে নির্দিষ্ট অংশ visualize করতে পারো।

```python
# যেসব মাসে Sales > 300
filtered = data[data["Sales"] > 300]

plt.bar(filtered["Month"], filtered["Sales"], color='green')
plt.title("Months with Sales > 300")
plt.show()
```

দারুণ! 🎨
আজ আমরা শিখব —

# 🧩 Advanced Styling (Colors, Themes, Annotations)

---

## 🎯 ১. কেন গ্রাফ সুন্দরভাবে স্টাইল করা জরুরি?

ডেটা visualization মানে শুধু চার্ট বানানো নয় —
বরং সেটিকে এমনভাবে উপস্থাপন করা, যেন **তথ্য এক নজরে বোঝা যায়**।
তাই আমরা শিখব কিভাবে গ্রাফে রঙ, থিম, ও নোট (annotation) যোগ করে তাকে **প্রেজেন্টেশন লেভেল**-এর মতো সুন্দর করা যায়।

---

## 🎨 ২. Color Customization 🎨

তুমি `color` প্যারামিটারে নিচের যেকোনোভাবে রঙ দিতে পারো:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]

# বিভিন্নভাবে রঙ দেওয়া যায়
plt.plot(x, y, color='purple', marker='o')          # নাম দিয়ে
# plt.plot(x, y, color='#FF5733', marker='o')       # Hex কোড দিয়ে
# plt.plot(x, y, color=(0.2, 0.8, 0.4), marker='o') # RGB tuple দিয়ে

plt.title("Custom Color Example")
plt.show()
```

✅ **Tip:** Hex রঙ ব্যবহার করলে অনেক সুন্দর ও নির্দিষ্ট রঙ পাওয়া যায় (যেমন: `#3498db`, `#e74c3c`)।

---

## 🧭 ৩. Matplotlib-এর Built-in Themes (Styles)

Matplotlib-এ অনেক সুন্দর থিম আগে থেকেই আছে।
তুমি শুধু `plt.style.use()` ব্যবহার করবে।

```python
plt.style.use('ggplot')
plt.plot(x, y, marker='o')
plt.title("Using ggplot Style")
plt.show()
```

📋 **জনপ্রিয় কিছু থিম:**

| Style Name                | Description                        |
| ------------------------- | ---------------------------------- |
| `'ggplot'`                | Modern look, inspired by R ggplot2 |
| `'seaborn-v0_8-darkgrid'` | হালকা গ্রিডসহ নরম ব্যাকগ্রাউন্ড    |
| `'bmh'`                   | Report-style                       |
| `'classic'`               | Default পুরোনো লুক                 |
| `'dark_background'`       | ডার্ক মোড থিম                      |

👉 **সব থিম দেখতে পারো:**

```python
print(plt.style.available)
```

---

## ✏️ ৪. Annotation (গ্রাফে নোট বা টেক্সট দেওয়া)

তুমি যেকোনো পয়েন্টে নোট বা টেক্সট দিতে পারো —
যেমন সর্বোচ্চ মান কোথায়, সেটা বোঝাতে 👇

```python
plt.style.use('seaborn-v0_8-darkgrid')

x = [1, 2, 3, 4, 5]
y = [10, 20, 15, 25, 30]

plt.plot(x, y, marker='o')
plt.title("Sales Growth")
plt.xlabel("Month")
plt.ylabel("Sales")

# Annotation যোগ করা
plt.annotate("Highest Point",
             xy=(5, 30), xytext=(3.5, 32),
             arrowprops=dict(facecolor='red', shrink=0.05))

plt.show()
```

🔹 এখানে:

- `xy` → যেখানে arrow যাবে
- `xytext` → টেক্সট কোথায় থাকবে
- `arrowprops` → তীরচিহ্নের স্টাইল

---

## 🌈 ৫. Background ও Grid Customize করা

```python
plt.figure(facecolor='#f8f9fa')  # ব্যাকগ্রাউন্ড রঙ

plt.plot(x, y, color='#2ecc71', linewidth=3)
plt.grid(color='gray', linestyle='--', linewidth=0.5)
plt.title("Styled Background & Grid")
plt.show()
```

✅ সুন্দর ব্যাকগ্রাউন্ড ও নরম grid লাইন presentation-এর জন্য চমৎকার লাগে।

---

## 🧱 ৬. Font ও Text Customization

তুমি font size, রঙ, style ইত্যাদি পরিবর্তন করতে পারো:

```python
plt.title("Sales Report", fontsize=16, color='navy', fontweight='bold')
plt.xlabel("Month", fontsize=12, color='darkred')
plt.ylabel("Revenue", fontsize=12, color='darkred')
```

---

## 💡 ৭. একাধিক থিম ও কাস্টম রঙ একত্রে

```python
plt.style.use('bmh')

plt.plot(x, y, color='#9b59b6', marker='D', linewidth=2, label='Product A')
plt.legend()
plt.title("Styled Graph Example", fontsize=14, color='darkblue')
plt.show()
```

🎨 এইভাবে তুমি presentation-ready চার্ট বানাতে পারো।

---

## 📋 ৮. আজ যা শিখলে

| বিষয়                      | কাজ                                       |
| ------------------------- | ----------------------------------------- |
| রঙ পরিবর্তন               | `color='blue'`, Hex, RGB                  |
| থিম সেট করা               | `plt.style.use('ggplot')`                 |
| Annotation যোগ করা        | `plt.annotate()`                          |
| Background ও Grid Control | `plt.figure(facecolor=...)`, `plt.grid()` |
| Font Style ও রঙ           | `fontsize`, `color`, `fontweight`         |

চমৎকার! 🎉
আজ আমরা এসেছি আমাদের **Matplotlib বাংলা কোর্সের শেষ পাঠে** —

# 🏆 Final Project – Real Data Visualization\*\*

## 🧠 প্রজেক্ট ধারণা

আমরা দেখব —
👉 “**বাংলাদেশে ৬ বছরে ইন্টারনেট ব্যবহারকারীর সংখ্যা কীভাবে বেড়েছে**”

আমরা এই ডেটা ধরব:

| বছর  | ব্যবহারকারী (মিলিয়ন) |
| ---- | -------------------- |
| 2018 | 80                   |
| 2019 | 90                   |
| 2020 | 100                  |
| 2021 | 120                  |
| 2022 | 130                  |
| 2023 | 150                  |

---

## 🧮 ধাপ ১: ডেটা তৈরি করা

```python
import matplotlib.pyplot as plt

# ডেটা
years = [2018, 2019, 2020, 2021, 2022, 2023]
users = [80, 90, 100, 120, 130, 150]
```

---

## 🎨 ধাপ ২: Line Graph তৈরি করা

```python
plt.figure(figsize=(8,5))
plt.plot(years, users, color='#3498db', marker='o', linewidth=3)

plt.title("বাংলাদেশে ইন্টারনেট ব্যবহারকারীর বৃদ্ধি (2018–2023)", fontsize=14, color='navy')
plt.xlabel("Year", fontsize=12)
plt.ylabel("Users (in Millions)", fontsize=12)
plt.grid(True)
plt.show()
```

📈 এটি দেখাবে সময়ের সাথে সাথে ইন্টারনেট ব্যবহারকারীর ধারাবাহিক বৃদ্ধি।

---

## 📊 ধাপ ৩: Bar Chart দিয়ে তুলনা

```python
plt.bar(years, users, color='skyblue', edgecolor='black')
plt.title("Internet Users by Year (Bar Chart)")
plt.xlabel("Year")
plt.ylabel("Users (in Millions)")
plt.show()
```

🔹 Bar Chart তুলনামূলকভাবে বুঝতে সাহায্য করে কোন বছর সবচেয়ে বেশি বৃদ্ধি হয়েছে।

---

## 🥧 ধাপ ৪: Pie Chart (Percentage অনুযায়ী)

```python
plt.pie(users, labels=years, autopct='%1.1f%%', startangle=90, shadow=True)
plt.title("Internet Usage Share by Year")
plt.show()
```

🎯 এতে প্রতিটি বছরের শতকরা ভাগ দেখা যাবে।

---

## ✏️ ধাপ ৫: Annotation যোগ করা

আমরা গ্রাফে “সবচেয়ে বেশি ব্যবহারকারীর বছর” (২০২৩) হাইলাইট করব 👇

```python
plt.plot(years, users, color='#2ecc71', marker='o')
plt.title("Internet User Growth in Bangladesh")
plt.xlabel("Year")
plt.ylabel("Users (in Millions)")

plt.annotate("Peak Year (150M)", xy=(2023,150), xytext=(2020,155),
             arrowprops=dict(facecolor='red', shrink=0.05))

plt.grid(True)
plt.show()
```

🔸 এখানে annotation দেখাবে যে ২০২৩ সালে সর্বাধিক ব্যবহারকারী ছিল।

---

## 🖼️ ধাপ ৬: একাধিক গ্রাফ একসাথে (Subplot)

```python
plt.figure(figsize=(10,5))

# Line Graph
plt.subplot(1, 2, 1)
plt.plot(years, users, color='blue', marker='o')
plt.title("Line Graph")

# Bar Graph
plt.subplot(1, 2, 2)
plt.bar(years, users, color='orange')
plt.title("Bar Graph")

plt.tight_layout()
plt.show()
```

এতে দুইটি ভিন্ন ধরনের গ্রাফ এক স্ক্রিনে দেখা যাবে।

---

## 📋 সারসংক্ষেপ (Final Review)

| কাজ             | ব্যবহৃত টুল / ফাংশন    |
| --------------- | ---------------------- |
| ডেটা লোড / তৈরি | List বা CSV            |
| লাইন গ্রাফ      | `plt.plot()`           |
| বার চার্ট       | `plt.bar()`            |
| পাই চার্ট       | `plt.pie()`            |
| এনোটেশন         | `plt.annotate()`       |
| একাধিক গ্রাফ    | `plt.subplot()`        |
| কাস্টম স্টাইল   | `plt.style.use()` + রঙ |
