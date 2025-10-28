# NumPy পরিচিতি
## 🧠 NumPy কী?

**NumPy** হলো **Numerical Python**-এর সংক্ষিপ্ত রূপ। এটি একটি **Python library** যা ব্যবহৃত হয় সংখ্যাগত (numerical) এবং বৈজ্ঞানিক (scientific) গণনার জন্য।
বিশেষ করে এটি **array** নিয়ে কাজ করার জন্য খুব শক্তিশালী ও দ্রুত।

---

## 🔢 NumPy কেন ব্যবহার করব?

Python-এর সাধারণ list দিয়ে আমরা ডেটা সংরক্ষণ করতে পারি, কিন্তু list-এ গণনা ধীর হয়।
NumPy-এর **array** list-এর মতো হলেও, এটি অনেক দ্রুত, কম মেমোরি ব্যবহার করে এবং ম্যাট্রিক্স / ভেক্টর গাণিতিক কাজ সহজ করে।

👉 উদাহরণ:

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
print(a)
print(a + 5)
print(a * 2)
```

**Output:**

```
[1 2 3 4 5]
[6 7 8 9 10]
[ 2  4  6  8 10]
```

---

## ⚙️ NumPy Array কী?

NumPy-এর প্রধান ডেটা স্ট্রাকচার হলো **ndarray (N-dimensional array)**।

### 🧩 এক-মাত্রিক Array:

```python
arr1 = np.array([1, 2, 3])
```

### 🧩 দুই-মাত্রিক Array (Matrix):

```python
arr2 = np.array([[1, 2, 3], [4, 5, 6]])
```

---

## 🧮 Array-এর কিছু দরকারি ফাংশন:

| Function              | কাজ                                           |
| --------------------- | --------------------------------------------- |
| `np.zeros(5)`         | সব মান 0 দিয়ে ভরা array তৈরি করে             |
| `np.ones((2,3))`      | 2x3 এর এক-ভরা array তৈরি করে                  |
| `np.arange(0,10,2)`   | 0 থেকে 10 পর্যন্ত 2 করে বৃদ্ধি পায় এমন array |
| `np.linspace(0,1,5)`  | 0 থেকে 1 পর্যন্ত 5টি সমান ব্যবধানের মান দেয়  |
| `np.random.rand(3,2)` | 3x2 random সংখ্যা তৈরি করে                    |
| `np.sum(arr)`         | array-এর সব উপাদানের যোগফল                    |
| `np.mean(arr)`        | গড় (average) বের করে                         |
| `np.shape(arr)`       | array-এর dimension জানায়                     |

চমৎকার! 😄
এখন আমরা শিখব — **NumPy-তে ndarray creation from scratch**, অর্থাৎ **পুরোপুরি নতুনভাবে (শূন্য থেকে) ndarray তৈরি করা**।

---
# ndarray Creation from Scratch
## 🧠 “From Scratch” মানে কী?

“From Scratch” মানে হলো —
আমরা কোনো existing list, tuple বা অন্য data ব্যবহার করছি না; বরং NumPy-এর **built-in functions** ব্যবহার করে একদম নতুন array তৈরি করছি।

এগুলো বিশেষ করে **initialization**, **testing**, বা **matrix operation** শেখার সময় খুব কাজে লাগে।

---

## 🔹 ১️⃣ `np.zeros()` — সব মান 0 দিয়ে ভরা array

```python
import numpy as np

arr = np.zeros((3, 4))   # 3 rows, 4 columns
print(arr)
```

**Output:**

```
[[0. 0. 0. 0.]
 [0. 0. 0. 0.]
 [0. 0. 0. 0.]]
```

👉 সব element-এর মান `0` এবং dtype ডিফল্টভাবে `float64` হয়।

---

## 🔹 ২️⃣ `np.ones()` — সব মান 1 দিয়ে ভরা array

```python
arr = np.ones((2, 3), dtype=int)
print(arr)
```

**Output:**

```
[[1 1 1]
 [1 1 1]]
```

> এখানে আমরা `dtype=int` ব্যবহার করেছি যাতে মানগুলো পূর্ণসংখ্যা থাকে।

---

## 🔹 ৩️⃣ `np.full()` — নির্দিষ্ট মান দিয়ে ভরা array

```python
arr = np.full((3, 3), 7)
print(arr)
```

**Output:**

```
[[7 7 7]
 [7 7 7]
 [7 7 7]]
```

> এটি তখন কাজে লাগে যখন একটি নির্দিষ্ট মান দিয়ে ম্যাট্রিক্স তৈরি করতে চাই।

---

## 🔹 ৪️⃣ `np.eye()` — Identity Matrix তৈরি করা

```python
arr = np.eye(4)
print(arr)
```

**Output:**

```
[[1. 0. 0. 0.]
 [0. 1. 0. 0.]
 [0. 0. 1. 0.]
 [0. 0. 0. 1.]]
```

> এটি একটি **square matrix** যেখানে diagonal-এর মান 1 এবং বাকি সব 0।

---

## 🔹 ৫️⃣ `np.arange()` — নির্দিষ্ট range-এর মধ্যে সংখ্যা তৈরি

```python
arr = np.arange(0, 10, 2)  # start, stop, step
print(arr)
```

**Output:**

```
[0 2 4 6 8]
```

> এটি `range()` ফাংশনের মতো কাজ করে, কিন্তু NumPy array তৈরি করে।

---

## 🔹 ৬️⃣ `np.linspace()` — সমান ব্যবধানের সংখ্যা তৈরি

```python
arr = np.linspace(0, 1, 5)  # start, end, total numbers
print(arr)
```

**Output:**

```
[0.   0.25 0.5  0.75 1.  ]
```

> এটি start ও end-এর মধ্যে নির্দিষ্ট সংখ্যক মান তৈরি করে (equally spaced)।

---

## 🔹 ৭️⃣ `np.random` — Random সংখ্যার array তৈরি

### 🧩 ক. `np.random.rand()` — 0 থেকে 1-এর মধ্যে random float সংখ্যা

```python
arr = np.random.rand(2, 3)
print(arr) # 2 rows, 3 columns of random floats
```

### 🧩 খ. `np.random.randint()` — নির্দিষ্ট range-এর random integer সংখ্যা

```python
arr = np.random.randint(10, 50, size=(3, 4))
print(arr) # Random integers between 10 and 50
```

---

## 🔹 ৮️⃣ `np.empty()` — Uninitialized array (random মান সহ)

```python
arr = np.empty((2, 3))
print(arr)
```

**Output:** (random garbage values)

```
[[1.232e-312 0.000e+000 2.121e-314]
 [4.940e-324 1.234e-321 0.000e+000]]
```

> এটি দ্রুত array তৈরি করে, কিন্তু মানগুলো initialize করে না (যতক্ষণ না আপনি overwrite করেন)।

---

## 🧮 সংক্ষেপে মনে রাখার মতো ফাংশন

| ফাংশন                                | কাজ                                |
| ------------------------------------ | ---------------------------------- |
| `np.zeros(shape)`                    | 0 দিয়ে ভরা array তৈরি করে         |
| `np.ones(shape)`                     | 1 দিয়ে ভরা array তৈরি করে         |
| `np.full(shape, value)`              | নির্দিষ্ট মান দিয়ে array তৈরি করে |
| `np.eye(n)`                          | Identity matrix তৈরি করে           |
| `np.arange(start, stop, step)`       | নির্দিষ্ট range-এর সংখ্যা তৈরি করে |
| `np.linspace(start, stop, num)`      | সমান ব্যবধানের মান তৈরি করে        |
| `np.random.rand(shape)`              | Random float সংখ্যা                |
| `np.random.randint(low, high, size)` | Random integer সংখ্যা              |
| `np.empty(shape)`                    | Uninitialized array                |

---

## ✅ সারসংক্ষেপ

* “From scratch” মানে কোনো existing data ব্যবহার না করে array তৈরি করা
* NumPy-এর built-in ফাংশনগুলো array initialization সহজ ও দ্রুত করে
* Random ও Identity matrix তৈরি করা যায় সহজেই


# ⚙️ ndarray-এর প্রধান Attributes (গুণাবলী)

NumPy-এর প্রতিটি array-এর কিছু গুরুত্বপূর্ণ attribute (বৈশিষ্ট্য) আছে, যেগুলো দিয়ে array সম্পর্কে বিভিন্ন তথ্য জানা যায়।

```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr)
```

**Output:**

```
[[1 2 3]
 [4 5 6]]
```

---



| Attribute          | কাজ                                                      | উদাহরণ                          |
| ------------------ | -------------------------------------------------------- | ------------------------------- |
| `ndarray.ndim`     | array-এর dimension সংখ্যা জানায়                         | `arr.ndim` → 2                  |
| `ndarray.shape`    | প্রতিটি dimension-এর আকার (rows, columns ইত্যাদি) জানায় | `arr.shape` → (2, 3)            |
| `ndarray.size`     | মোট উপাদান (elements)-এর সংখ্যা জানায়                   | `arr.size` → 6                  |
| `ndarray.dtype`    | উপাদানগুলোর data type জানায়                             | `arr.dtype` → int64             |
| `ndarray.itemsize` | প্রতিটি উপাদান কত byte জায়গা নিচ্ছে তা জানায়           | `arr.itemsize` → 8              |
| `ndarray.nbytes`   | পুরো array মোট কত byte জায়গা নিচ্ছে তা জানায়           | `arr.nbytes` → 48               |
| `ndarray.T`        | array-এর transpose দেয় (row ↔ column পরিবর্তন)          | `arr.T` → `[[1,4],[2,5],[3,6]]` |

---

### 🧩 উদাহরণ:

```python
import numpy as np

arr = np.array([[1, 2, 3],
                [4, 5, 6]])

print("Array:\n", arr)
print("Dimension (ndim):", arr.ndim)
print("Shape:", arr.shape)
print("Size:", arr.size)
print("Data type (dtype):", arr.dtype)
print("Item size:", arr.itemsize)
print("Total bytes:", arr.nbytes)
print("Transpose:\n", arr.T)
```

**Output:**

```
Array:
 [[1 2 3]
 [4 5 6]]
Dimension (ndim): 2
Shape: (2, 3)
Size: 6
Data type (dtype): int64
Item size: 8
Total bytes: 48
Transpose:
 [[1 4]
 [2 5]
 [3 6]]
```



## 📘 সংক্ষেপে মনে রাখার মতো বিষয়:

* `ndim` → dimension সংখ্যা
* `shape` → প্রতিটি dimension-এর আকার
* `size` → মোট উপাদান সংখ্যা
* `dtype` → data type
* `itemsize` → প্রতিটি উপাদানের byte
* `nbytes` → মোট memory size
* `T` → Transpose (row ↔ column পরিবর্তন)


# ⚡ কেন NumPy দ্রুত?

NumPy-এর array-গুলো **C language-এ optimized** হয়ে তৈরি, তাই Python list-এর তুলনায় এটি অনেক দ্রুত কাজ করে।
এছাড়াও এটি **vectorized operations** সমর্থন করে (যেমন পুরো array-এর উপর একসাথে অপারেশন চালানো যায়)।

---

## 📊 ছোট একটি উদাহরণ:

```python
import numpy as np

data = np.array([[1, 2, 3],
                 [4, 5, 6]])

print("Shape:", data.shape)# (2, 3 => 2 rows, 3 columns)
print("Sum:", np.sum(data))# 21
print("Column Sum:", np.sum(data, axis=0)) # [5 7 9]
print("Row Sum:", np.sum(data, axis=1)) # [ 6 15]
```

---

## 🧩 সংক্ষেপে NumPy-এর উপকারিতা:

* দ্রুত ও কার্যকর গণনা (Fast computation)
* কম মেমোরি ব্যবহার
* Multidimensional array সমর্থন
* Mathematical ও statistical operations সহজ
* Machine Learning, Data Science, ও AI-এর ভিত্তি

---

# NumPy ডেটা টাইপ (Data Types)

## 🧠 Ndarray Data Type কী?

NumPy array বা **ndarray**-এর সব উপাদান (elements) **একই ধরনের data type** ধারণ করে।
এই data type কে বলা হয় **`dtype` (data type object)**।

👉 অর্থাৎ, একটি ndarray-তে সব উপাদান integer হলে সেটার dtype হবে `int32` বা `int64`, আর যদি float হয় তাহলে হবে `float64` ইত্যাদি।

---

## 🔢 সাধারণ NumPy Data Types

| ডেটা টাইপ                             | বর্ণনা                                           | উদাহরণ               |
| ------------------------------------- | ------------------------------------------------ | -------------------- |
| `int8`, `int16`, `int32`, `int64`     | Signed integer (negative ও positive উভয় সংখ্যা) | `-5, 0, 12`          |
| `uint8`, `uint16`, `uint32`, `uint64` | Unsigned integer (শুধু positive সংখ্যা)          | `0, 5, 10`           |
| `float16`, `float32`, `float64`       | Floating-point সংখ্যা (দশমিক সহ)                 | `3.14, -2.5`         |
| `complex64`, `complex128`             | Complex সংখ্যা (real + imaginary)                | `2 + 3j`             |
| `bool_`                               | Boolean মান (True / False)                       | `True`, `False`      |
| `str_`, `unicode_`                    | String ডেটা                                      | `"Hello"`, `'World'` |

---

## 🧩 উদাহরণসহ ব্যাখ্যা

```python
import numpy as np

# Integer array
a = np.array([1, 2, 3, 4])
print(a.dtype)   # int64 (depends on system)

# Float array
b = np.array([1.2, 3.4, 5.6])
print(b.dtype)   # float64

# Boolean array
c = np.array([True, False, True])
print(c.dtype)   # bool

# String array
d = np.array(["Mamun", "NumPy"])
print(d.dtype)   # <U5 (Unicode string of length 5)
```

---

## ⚙️ dtype পরিবর্তন (Type Conversion)

NumPy-তে array-এর data type সহজেই পরিবর্তন করা যায় `astype()` মেথড দিয়ে।

```python
arr = np.array([1.5, 2.8, 3.9])
print("Original dtype:", arr.dtype)

# Convert to int
arr_int = arr.astype(int)
print("After conversion:", arr_int)
print("New dtype:", arr_int.dtype)
```

**Output:**

```
Original dtype: float64
After conversion: [1 2 3]
New dtype: int64
```

---

## 🧮 dtype নির্ধারণ করে array তৈরি করা

তুমি চাইলে array তৈরি করার সময়ও dtype নির্দিষ্ট করে দিতে পারো।

```python
arr = np.array([1, 2, 3], dtype=float)
print(arr)
print(arr.dtype)
```

**Output:**

```
[1. 2. 3.]
float64
```

---

## 📘 সংক্ষেপে মনে রাখার মতো বিষয়

* ndarray-এর সব উপাদান একই data type ধারণ করে
* `dtype` attribute দিয়ে data type জানা যায়
* `astype()` দিয়ে data type পরিবর্তন করা যায়
* Data type নির্দিষ্ট করে array তৈরি করা যায়

# ndarray Creation from Existing Data
## 🧠 ndarray Creation from Existing Data মানে কী?

এর মানে হলো —
আমরা **Python-এর বিদ্যমান ডেটা স্ট্রাকচার (যেমন list, tuple, বা অন্য ndarray)** ব্যবহার করে নতুন **NumPy array (`ndarray`)** তৈরি করব।

NumPy-তে এটি করা হয় `np.array()` ফাংশনের মাধ্যমে।

---

## 🔹 ১️⃣ Python List থেকে ndarray তৈরি করা

Python list হলো সবচেয়ে সাধারণ উৎস।
তুমি সহজেই একটি list কে NumPy array-এ রূপান্তর করতে পারো।

```python
import numpy as np

# One-dimensional list
list1 = [1, 2, 3, 4, 5]
arr1 = np.array(list1)
print("Array from list:", arr1)
```

**Output:**

```
Array from list: [1 2 3 4 5]
```

---

## 🔹 ২️⃣ Nested List (2D list) থেকে 2D ndarray তৈরি করা

Nested list মানে লিস্টের ভিতরে লিস্ট — অর্থাৎ ম্যাট্রিক্সের মতো গঠন।

```python
data = [[1, 2, 3],
        [4, 5, 6]]

arr2 = np.array(data)
print("2D Array:\n", arr2)
```

**Output:**

```
2D Array:
 [[1 2 3]
  [4 5 6]]
```

---

## 🔹 ৩️⃣ Tuple থেকে ndarray তৈরি করা

Tuple থেকেও সরাসরি array বানানো যায়।

```python
tup = (10, 20, 30)
arr3 = np.array(tup)
print("Array from tuple:", arr3)
```

**Output:**

```
Array from tuple: [10 20 30]
```

---

## 🔹 ৪️⃣ Existing ndarray থেকে নতুন ndarray তৈরি করা

কখনও কখনও আমরা একটি পুরনো array থেকে নতুন array বানাতে চাই — যেমন copy বা conversion।

### 🧩 ক. Copy তৈরি করা:

```python
arr = np.array([1, 2, 3])
new_arr = np.array(arr)
print("New array:", new_arr)
```

> এটি মূল array-এর একটি **independent copy** তৈরি করে।

---

### 🧩 খ. ভিন্ন dtype-এ রূপান্তর:

```python
arr = np.array([1, 2, 3])
float_arr = np.array(arr, dtype=float)
print(float_arr)
```

**Output:**

```
[1. 2. 3.]
```

---

## 🔹 ৫️⃣ Mixed Type থেকে ndarray তৈরি করা

যদি list বা tuple-এ বিভিন্ন ধরনের data থাকে (যেমন সংখ্যা + string),
NumPy সেটিকে **সবচেয়ে general type (যেমন string)** এ convert করে ফেলে।

```python
arr = np.array([1, 2, '3'])
print(arr)
print(arr.dtype)
```

**Output:**

```
['1' '2' '3']
<U11
```

> 🔍 এখানে সব মান string টাইপে রূপান্তর হয়েছে।

---

## ⚙️ সংক্ষেপে ndarray তৈরির উপায়

| উৎস (Source)     | উদাহরণ              | ফাংশন                           |
| ---------------- | ------------------- | ------------------------------- |
| List             | `[1, 2, 3]`         | `np.array(list)`                |
| Nested List      | `[[1,2,3],[4,5,6]]` | `np.array(list)`                |
| Tuple            | `(1,2,3)`           | `np.array(tuple)`               |
| Existing ndarray | `np.array(old_arr)` | নতুন copy তৈরি করে              |
| Mixed Type       | `[1, '2', 3.0]`     | সবকিছুকে একই টাইপে রূপান্তর করে |

---

## ✅ সংক্ষিপ্ত সারসংক্ষেপ

* Existing data থেকে ndarray তৈরি করা যায় `np.array()` ফাংশন ব্যবহার করে
* dtype স্বয়ংক্রিয়ভাবে নির্ধারিত হয়, তবে চাইলে তুমি নিজে `dtype=` দিয়ে নির্দিষ্ট করতে পারো
* Nested list থেকে 2D / 3D array বানানো যায়
* Existing ndarray থেকেও নতুন ndarray তৈরি করা সম্ভব

চমৎকার! 😄
এখন আমরা শিখব — **NumPy-তে কীভাবে random মান (random values)** দিয়ে **ndarray তৈরি করা যায়**।
এটা খুবই গুরুত্বপূর্ণ কারণ **data analysis, simulation, machine learning, testing** — সব ক্ষেত্রেই random array দরকার হয়।

---

## 🎲 NumPy Random Module পরিচিতি

NumPy-এর মধ্যে একটি submodule আছে —
👉 **`numpy.random`**

এই মডিউল ব্যবহার করে আমরা বিভিন্ন ধরনের random সংখ্যা (integer, float, normal distribution ইত্যাদি) তৈরি করতে পারি।

---

## 🔹 ১️⃣ `np.random.rand()` — 0 থেকে 1-এর মধ্যে random float সংখ্যা

এই ফাংশন **uniform distribution** থেকে random float সংখ্যা তৈরি করে।

```python
import numpy as np

arr = np.random.rand(2, 3)
print(arr)
```

**Output (প্রতি রানেই ভিন্ন হবে):**

```
[[0.25 0.87 0.56]
 [0.12 0.98 0.44]]
```

👉 এখানে সব মান 0 এবং 1-এর মধ্যে float।

---

## 🔹 ২️⃣ `np.random.randn()` — Normal (Gaussian) distribution থেকে random সংখ্যা

এটি **mean = 0** এবং **standard deviation = 1** যুক্ত normal distribution থেকে সংখ্যা তৈরি করে।

```python
arr = np.random.randn(3, 2)
print(arr)
```

**Output (প্রতি রানেই আলাদা):**

```
[[-0.23  1.45]
 [ 0.67 -0.91]
 [ 1.23  0.12]]
```

> 🧠 এই distribution সাধারণত machine learning ও statistics-এ ব্যবহৃত হয়।

---

## 🔹 ৩️⃣ `np.random.randint()` — নির্দিষ্ট range-এর মধ্যে random integer সংখ্যা

```python
arr = np.random.randint(10, 50, size=(3, 4))
print(arr)
```

**Output:**

```
[[37 11 45 22]
 [14 28 39 49]
 [12 43 30 18]]
```

👉 এখানে মানগুলো 10 থেকে 49 এর মধ্যে integer, এবং shape (3×4)।

---

## 🔹 ৪️⃣ `np.random.random()` — 0 থেকে 1-এর মধ্যে random float সংখ্যা (rand-এর বিকল্প)

```python
arr = np.random.random((2, 2))
print(arr)
```

**Output:**

```
[[0.56 0.89]
 [0.12 0.34]]
```

> এটি `np.random.rand()` এর মতোই কাজ করে, শুধু shape argument হিসেবে tuple নিতে হয়।

---

## 🔹 ৫️⃣ `np.random.choice()` — নির্দিষ্ট array থেকে random মান বেছে নেওয়া

```python
arr = np.random.choice([10, 20, 30, 40, 50], size=(2, 3))
print(arr)
```

**Output:**

```
[[40 10 20]
 [50 30 10]]
```

👉 এটি দেয়া তালিকা (list) বা array থেকে random ভাবে মান বেছে নেয়।

---

## 🔹 ৬️⃣ `np.random.uniform()` — নির্দিষ্ট range-এর মধ্যে random float

```python
arr = np.random.uniform(5, 10, size=(2, 3))
print(arr)
```

**Output:**

```
[[7.23 5.11 9.48]
 [6.88 8.33 5.72]]
```

> 5 থেকে 10-এর মধ্যে float মান তৈরি করে (uniform distribution)।

---

## 🔹 ৭️⃣ `np.random.normal()` — Normal distribution (mean ও std নির্ধারণ করা যায়)

```python
arr = np.random.normal(loc=50, scale=10, size=(3, 3))
print(arr)
```

**Output (প্রতি রানেই ভিন্ন):**

```
[[47.1 62.5 51.3]
 [42.7 55.2 60.1]
 [48.9 39.8 59.4]]
```

> এখানে `loc` = mean (গড়), `scale` = standard deviation, `size` = shape।

---

## 🧩 Random seed নির্ধারণ করা (reproducible ফলাফলের জন্য)

Random মান প্রতিবার পরিবর্তিত হয়, কিন্তু কখনও তুমি চাইবে **একই random মান পুনরায় পেতে**।
এর জন্য `np.random.seed()` ব্যবহার করা হয়।

```python
np.random.seed(42)
arr = np.random.randint(0, 10, (2, 3))
print(arr)
```

**Output (সবসময় একই থাকবে):**

```
[[6 3 7]
 [4 6 9]]
```

---

## 📘 সারসংক্ষেপ টেবিল

| ফাংশন                                | কাজ                                 | মানের ধরন |
| ------------------------------------ | ----------------------------------- | --------- |
| `np.random.rand()`                   | 0–1 এর মধ্যে random float           | Uniform   |
| `np.random.randn()`                  | Normal distribution (mean=0, std=1) | Gaussian  |
| `np.random.randint(a, b, size)`      | a থেকে b-এর মধ্যে random integer    | Integer   |
| `np.random.random(size)`             | 0–1 এর মধ্যে random float           | Uniform   |
| `np.random.uniform(low, high, size)` | নির্দিষ্ট range-এর float            | Uniform   |
| `np.random.choice(list, size)`       | নির্দিষ্ট তালিকা থেকে random মান    | Discrete  |
| `np.random.normal(loc, scale, size)` | Mean ও Std সহ normal distribution   | Gaussian  |

---

## ✅ সংক্ষেপে মনে রাখার বিষয়

* Random array তৈরি করার জন্য `numpy.random` মডিউল ব্যবহার হয়
* `rand()`, `randn()`, `random()`, `randint()` সবচেয়ে বেশি ব্যবহৃত
* `seed()` দিয়ে একই random ফলাফল পুনরায় তৈরি করা যায়

# NumPy Indexing and Slicing (বাংলায় উদাহরণসহ)

## 🧠 Indexing এবং Slicing কী?

* **Indexing** মানে হলো array-এর নির্দিষ্ট **একটি উপাদান (element)**-এ প্রবেশ করা।
* **Slicing** মানে হলো array-এর **একটি অংশ (range of elements)** নির্বাচন করা।

👉 ঠিক যেমন Python-এর list-এ আমরা করি:

```python
list1 = [10, 20, 30, 40]
print(list1[1:3])   # [20, 30]
```

NumPy-তে একই ধারণা, কিন্তু আরও শক্তিশালীভাবে কাজ করে!

---

## 🔹 ১️⃣ 1D Array Indexing

```python
import numpy as np

arr = np.array([10, 20, 30, 40, 50])
print(arr[0])   # প্রথম উপাদান
print(arr[-1])  # শেষ উপাদান
```

**Output:**

```
10
50
```

> `arr[index]` দিয়ে একক উপাদান নেওয়া যায়।

---

## 🔹 ২️⃣ 1D Array Slicing

```python
print(arr[1:4])   # index 1 থেকে 3 পর্যন্ত
print(arr[:3])    # শুরু থেকে index 2 পর্যন্ত
print(arr[2:])    # index 2 থেকে শেষ পর্যন্ত
print(arr[::2])   # প্রতি 2 স্টেপে একবার
```

**Output:**

```
[20 30 40]
[10 20 30]
[30 40 50]
[10 30 50]
```

---

## 🔹 ৩️⃣ 2D Array Indexing

```python
arr = np.array([[10, 20, 30],
                [40, 50, 60],
                [70, 80, 90]])

print(arr[0, 0])   # প্রথম সারির প্রথম উপাদান
print(arr[1, 2])   # দ্বিতীয় সারির তৃতীয় উপাদান
```

**Output:**

```
10
60
```

👉 সিনট্যাক্স: `arr[row_index, column_index]`

---

## 🔹 ৪️⃣ 2D Array Slicing

```python
print(arr[0:2, 1:3])   # প্রথম 2 সারি, কলাম 1 থেকে 2 পর্যন্ত
print(arr[:, 0])       # সব সারির প্রথম কলাম
print(arr[1, :])       # দ্বিতীয় সারির সব কলাম
```

**Output:**

```
[[20 30]
 [50 60]]

[10 40 70]

[40 50 60]
```

> `:` চিহ্ন ব্যবহার করা হয় "সবগুলো" বোঝাতে।

---

## 🔹 ৫️⃣ Negative Indexing (শেষ দিক থেকে গণনা)

```python
print(arr[-1])       # শেষ সারি
print(arr[-1, -2])   # শেষ সারির দ্বিতীয় উপাদান
```

**Output:**

```
[70 80 90]
80
```

---

## 🔹 ৬️⃣ Boolean Indexing (শর্ত অনুযায়ী মান নির্বাচন)

```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[arr > 25])   # ২৫-এর বেশি মানগুলো নাও
```

**Output:**

```
[30 40 50]
```

> এটি ডেটা ফিল্টারিং-এ খুব কার্যকর।

---

## 🔹 ৭️⃣ Fancy Indexing (ইন্ডেক্সের array দিয়ে নির্বাচন)

```python
arr = np.array([10, 20, 30, 40, 50])
index = [0, 2, 4]
print(arr[index])   # index 0, 2, 4 এর মান নাও
```

**Output:**

```
[10 30 50]
```

---

## 🔹 ৮️⃣ 2D Fancy Indexing

```python
arr = np.array([[10, 20, 30],
                [40, 50, 60],
                [70, 80, 90]])

rows = [0, 2]
cols = [1, 2]
print(arr[rows, cols])
```

**Output:**

```
[20 90]
```

👉 এখানে `(0,1)` এবং `(2,2)` পজিশনের মান নেওয়া হয়েছে।

---

## 🧩 ৯️⃣ Array Slice পরিবর্তনযোগ্য (Mutable)

Python list-এর মতো NumPy slice কপি তৈরি করে না — বরং মূল array-এর **view** দেয়।
মানে slice পরিবর্তন করলে মূল array-ও পরিবর্তিত হয়।

```python
arr = np.array([1, 2, 3, 4, 5])
sub = arr[1:4]
sub[0] = 99

print("Sub:", sub)
print("Original:", arr)
```

**Output:**

```
Sub: [99  3  4]
Original: [ 1 99  3  4  5]
```

> ⚠️ তাই slice ব্যবহার করার সময় সাবধান থাকতে হবে।

---

## 📘 সংক্ষিপ্ত সারসংক্ষেপ

| ধরন               | উদাহরণ         | ব্যাখ্যা               |
| ----------------- | -------------- | ---------------------- |
| Simple Indexing   | `arr[2]`       | একক মান                |
| 2D Indexing       | `arr[1,2]`     | row 1, col 2           |
| Slicing           | `arr[1:4]`     | অংশবিশেষ               |
| Step Slice        | `arr[::2]`     | প্রতি 2 ধাপে একবার     |
| Boolean Indexing  | `arr[arr>10]`  | শর্ত অনুযায়ী মান      |
| Fancy Indexing    | `arr[[0,2,4]]` | একাধিক নির্দিষ্ট index |
| Negative Indexing | `arr[-1]`      | শেষ দিক থেকে নির্বাচন  |

---

## ✅ সারসংক্ষেপে মনে রাখো

* NumPy-তে Indexing ও Slicing খুবই শক্তিশালী এবং দ্রুত
* Slice মূল array-এর view, তাই পরিবর্তন করলে আসল array-ও বদলায়
* Boolean ও Fancy indexing ডেটা ফিল্টারিং-এর জন্য দারুণ কার্যকর

# NumPy Copy vs View (বাংলায় উদাহরণসহ)

## 🧠 ১️⃣ ndarray Copy (কপি তৈরি করা)

NumPy-তে দুটি ধরনের কপি করা যায় —

* **View (Shallow Copy)**
* **Copy (Deep Copy)**

---

### 🔹 A. View — `arr.view()`

এটি মূল array-এর সাথে **data share করে**, অর্থাৎ একটিতে পরিবর্তন করলে অন্যটাতেও প্রভাব পড়ে।

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
view_arr = arr.view()

view_arr[0] = 99

print("Original:", arr)
print("View:", view_arr)
```

**Output:**

```
Original: [99  2  3  4  5]
View: [99  2  3  4  5]
```

> ⚠️ View শুধু “নতুন দৃষ্টি” দেয়, আলাদা ডেটা নয়।

---

### 🔹 B. Copy — `arr.copy()`

এটি সম্পূর্ণ নতুন array তৈরি করে।
মূল array পরিবর্তন করলে কপিতে কোনো প্রভাব পড়ে না।

```python
arr = np.array([10, 20, 30])
copy_arr = arr.copy()

copy_arr[0] = 999

print("Original:", arr)
print("Copy:", copy_arr)
```

**Output:**

```
Original: [10 20 30]
Copy: [999  20  30]
```

> ✅ এটি স্বাধীন (independent) কপি।

---

## 🧩 সারসংক্ষেপ (Copy vs View)

| বিষয়                                  | View         | Copy         |
| ------------------------------------- | ------------ | ------------ |
| Data শেয়ার করে?                       | ✅ হ্যাঁ      | ❌ না         |
| Memory আলাদা?                         | ❌ না         | ✅ হ্যাঁ      |
| একটিতে পরিবর্তন করলে অন্যটিতে প্রভাব? | ✅ হ্যাঁ      | ❌ না         |
| তৈরি হয় কিভাবে?                       | `arr.view()` | `arr.copy()` |

---


# Iteration in NumPy Arrays (বাংলায় উদাহরণসহ)
## 🔁  Iteration (Array-এর উপর লুপ চালানো)

NumPy array-এর উপর `for` লুপ চালিয়ে সহজেই প্রতিটি উপাদানে কাজ করা যায়।

---

### 🔹 A. 1D Array Iteration

```python
arr = np.array([10, 20, 30])
for x in arr:
    print(x)
```

**Output:**

```
10
20
30
```

---

### 🔹 B. 2D Array Iteration (Row by Row)

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

for row in arr:
    print(row)
```

**Output:**

```
[1 2 3]
[4 5 6]
```

---

### 🔹 C. Nested Loop (Element by Element)

```python
for row in arr:
    for item in row:
        print(item, end=' ')
```

**Output:**

```
1 2 3 4 5 6
```

---

### 🔹 D. Flat Iteration — `np.nditer()`

`nditer()` দিয়ে সহজভাবে পুরো multidimensional array একবারে ইটারেট করা যায়।

```python
arr = np.array([[10, 20],
                [30, 40],
                [50, 60]])

for x in np.nditer(arr):
    print(x, end=' ')
```

**Output:**

```
10 20 30 40 50 60
```

---

### 🔹 E. Enumerated Iteration — `np.ndenumerate()`

এটি index সহ মান দেয়।

```python
for idx, val in np.ndenumerate(arr):
    print(idx, val)
```

**Output:**

```
(0, 0) 10
(0, 1) 20
(1, 0) 30
(1, 1) 40
(2, 0) 50
(2, 1) 60
```

> 🧠 এটি array traversal বা debugging-এর সময় কাজে লাগে।

---

## 📘 সংক্ষিপ্ত সারসংক্ষেপ

| বিষয়             | ফাংশন / সিনট্যাক্স    | কাজ                           |
| ---------------- | --------------------- | ----------------------------- |
| Shallow Copy     | `arr.view()`          | ডেটা শেয়ার করে                |
| Deep Copy        | `arr.copy()`          | আলাদা ডেটা কপি তৈরি করে       |
| Integer Indexing | `arr[[1,3,4]]`        | একাধিক মান নির্বাচন           |
| Boolean Indexing | `arr[arr>5]`          | শর্ত অনুযায়ী ফিল্টার          |
| Fancy Indexing   | `arr[[0,2],[1,3]]`    | একাধিক row-col নির্বাচন       |
| Iteration        | `for x in arr:`       | উপাদান ধরে লুপ চালানো         |
| nditer()         | `np.nditer(arr)`      | সব element একবারে iterate করা |
| ndenumerate()    | `np.ndenumerate(arr)` | index + value সহ iteration    |

---

## ✅ সারসংক্ষেপে মনে রাখো

* `.copy()` → আলাদা কপি তৈরি করে
* `.view()` → একই ডেটা ভাগাভাগি করে
* Advanced Indexing ও Boolean Indexing দিয়ে নির্দিষ্ট মান বেছে নেওয়া যায়
* `np.nditer()` ও `np.ndenumerate()` array traversal সহজ করে

# NumPy ndarray Manipulation (বাংলায় উদাহরণসহ)

## 🧠 ndarray Manipulation কী?

**Manipulation** মানে হলো array-কে পরিবর্তন করা —
যেমন তার **আকার (shape)**, **dimension**, বা **orientation** বদলানো, কিন্তু ডেটা একই রাখা।

---

## 🔹 ১️⃣ `reshape()` — array-এর shape পরিবর্তন করা

`reshape()` ফাংশন ব্যবহার করে আমরা array-এর আকার পরিবর্তন করতে পারি (যতক্ষণ না total elements একই থাকে)।

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5, 6])
reshaped = arr.reshape(2, 3)
print(reshaped)
```

**Output:**

```
[[1 2 3]
 [4 5 6]]
```

👉 এখানে 1D array (6 elements) কে 2x3 আকারে রূপান্তর করা হয়েছে।

---

### ⚠️ নিয়ম:

* মোট উপাদান (elements) সংখ্যা একই থাকতে হবে।
  যেমন: 6 elements থাকলে `(2, 3)` বা `(3, 2)` করা যাবে, কিন্তু `(2, 4)` নয়।

---

## 🔹 ২️⃣ `reshape(-1)` — Automatically Flatten (1D তে পরিণত করা)

`-1` দিলে NumPy নিজে থেকেই বাকি dimension বের করে নেয়।

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

flat = arr.reshape(-1)
print(flat)
```

**Output:**

```
[1 2 3 4 5 6]
```

> 🧠 `-1` হলো একটি shorthand — অর্থাৎ “আমার জন্য dimension হিসাব করে দাও”।

---

## 🔹 ৩️⃣ `flatten()` — পুরো array কে 1D তে রূপান্তর

```python
arr = np.array([[10, 20],
                [30, 40],
                [50, 60]])

flat = arr.flatten()
print(flat)
```

**Output:**

```
[10 20 30 40 50 60]
```

> ✅ এটি একটি **copy** তৈরি করে (মূল array পরিবর্তন হয় না)।

---

## 🔹 ৪️⃣ `ravel()` — Flatten এর মতো, কিন্তু view দেয়

```python
arr = np.array([[1, 2], [3, 4]])
r = arr.ravel()
r[0] = 99

print("Ravel:", r)
print("Original:", arr)
```

**Output:**

```
Ravel: [99  2  3  4]
Original: [[99  2]
 [ 3  4]]
```

> ⚠️ `ravel()` মূল array-এর view দেয়, তাই এতে পরিবর্তন করলে আসল array-ও বদলায়।

---

## 🔹 ৫️⃣ `transpose()` — Row ↔ Column অদলবদল করা

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

trans = arr.transpose()
print(trans)
```

**Output:**

```
[[1 4]
 [2 5]
 [3 6]]
```

👉 Row গুলো এখন column হয়েছে (এবং উল্টোটা)।

---

## 🔹 ৬️⃣ `.T` Attribute — Transpose করার শর্টকাট

```python
arr = np.array([[10, 20, 30],
                [40, 50, 60]])
print(arr.T)
```

**Output:**

```
[[10 40]
 [20 50]
 [30 60]]
```

> `.T` হলো `transpose()` এর সংক্ষিপ্ত রূপ।

---

## 🔹 ৭️⃣ `resize()` — array-এর shape স্থায়ীভাবে পরিবর্তন করা

`reshape()` কেবল view দেয়, কিন্তু `resize()` মূল array-এর shape-ই বদলে দেয়।

```python
arr = np.array([1, 2, 3, 4, 5, 6])
arr.resize(2, 3)
print(arr)
```

**Output:**

```
[[1 2 3]
 [4 5 6]]
```

> ⚠️ এটি **in-place operation**, অর্থাৎ মূল array পরিবর্তিত হয়।

---

## 🔹 ৮️⃣ `np.newaxis` — Dimension বাড়ানো

1D array কে 2D বানাতে `np.newaxis` ব্যবহার করা হয়।

```python
arr = np.array([1, 2, 3, 4])
row_vec = arr[np.newaxis, :]  # row vector
col_vec = arr[:, np.newaxis]  # column vector

print("Row Vector:", row_vec)
print("Column Vector:\n", col_vec)
```

**Output:**

```
Row Vector: [[1 2 3 4]]
Column Vector:
 [[1]
 [2]
 [3]
 [4]]
```

> 🧠 এটি broadcasting এবং matrix operation-এ খুব দরকারি।

---

## 📘 সংক্ষিপ্ত সারসংক্ষেপ

| ফাংশন                | কাজ                             | কপি তৈরি করে?   |
| -------------------- | ------------------------------- | --------------- |
| `reshape()`          | shape পরিবর্তন করে              | ❌ না (view দেয়) |
| `reshape(-1)`        | Flatten করে                     | ❌ না            |
| `flatten()`          | 1D array তৈরি করে               | ✅ হ্যাঁ         |
| `ravel()`            | Flatten করে (view দেয়)          | ❌ না            |
| `transpose()` / `.T` | Row ↔ Column বদলায়              | ❌ না            |
| `resize()`           | মূল array-এর shape পরিবর্তন করে | ✅ হ্যাঁ         |
| `np.newaxis`         | নতুন dimension যোগ করে          | ✅ হ্যাঁ         |

---

## ✅ সারসংক্ষেপে মনে রাখো

* `reshape()` → আকার বদলায়, কিন্তু ডেটা অপরিবর্তিত
* `flatten()` → 1D কপি তৈরি করে
* `ravel()` → view দেয় (মূল array পরিবর্তিত হয়)
* `transpose()` / `.T` → Row ও Column অদলবদল
* `resize()` → shape স্থায়ীভাবে বদলায়
* `np.newaxis` → dimension যোগ করতে ব্যবহৃত হয়



## 🧠 ১️⃣ Array Stacking (Join / Merge)

**Stacking** মানে হলো একাধিক array-কে একত্র করা (join করা)।
NumPy-তে এটি করার জন্য অনেকগুলো ফাংশন আছে — যেমন:
`concatenate()`, `hstack()`, `vstack()`, `dstack()`, `column_stack()` ইত্যাদি।

---

### 🔹 (A) `np.concatenate()`

একই shape-এর array-গুলোকে একটি dimension-এ জোড়া লাগাতে ব্যবহৃত হয়।

```python
import numpy as np

a = np.array([[1, 2],
              [3, 4]])

b = np.array([[5, 6],
              [7, 8]])

res = np.concatenate((a, b), axis=0)
print(res)
```

**Output (axis=0 → vertically join):**

```
[[1 2]
 [3 4]
 [5 6]
 [7 8]]
```

👉 `axis=0` মানে নিচে নিচে যোগ হবে
👉 `axis=1` দিলে পাশাপাশিও যোগ করা যায়:

```python
np.concatenate((a, b), axis=1)
```

**Output:**

```
[[1 2 5 6]
 [3 4 7 8]]
```

---

### 🔹 (B) `np.vstack()` — Vertically stack (উপর নিচে যোগ)

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

res = np.vstack((a, b))
print(res)
```

**Output:**

```
[[1 2 3]
 [4 5 6]]
```

> Vertical = Row-wise যোগ করা।

---

### 🔹 (C) `np.hstack()` — Horizontally stack (পাশাপাশি যোগ)

```python
a = np.array([[1], [2], [3]])
b = np.array([[4], [5], [6]])

res = np.hstack((a, b))
print(res)
```

**Output:**

```
[[1 4]
 [2 5]
 [3 6]]
```

> Horizontal = Column-wise যোগ করা।

---

### 🔹 (D) `np.dstack()` — Depth-wise stack (3rd dimension এ যোগ)

```python
a = np.array([[1, 2],
              [3, 4]])

b = np.array([[5, 6],
              [7, 8]])

res = np.dstack((a, b))
print(res)
```

**Output:**

```
[[[1 5]
  [2 6]]
 [[3 7]
  [4 8]]]
```

> এখন array-এর dimension 3D (depth যোগ হয়েছে)।

---

### 🔹 (E) `np.column_stack()` — Columns হিসেবে যোগ করা

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

res = np.column_stack((a, b))
print(res)
```

**Output:**

```
[[1 4]
 [2 5]
 [3 6]]
```

> এটি 1D array গুলোকে 2D তে column-wise যোগ করে।

---

## 🧩 ২️⃣ Array Splitting (ভাগ করা)

**Splitting** মানে হলো একটি বড় array-কে ছোট ছোট অংশে ভাগ করা।

---

### 🔹 (A) `np.split()`

```python
arr = np.array([10, 20, 30, 40, 50, 60])
res = np.split(arr, 3)
print(res)
```

**Output:**

```
[array([10, 20]), array([30, 40]), array([50, 60])]
```

👉 এখানে array-কে 3 সমান ভাগে ভাগ করা হয়েছে।

---

### 🔹 (B) `np.hsplit()` — Horizontally Split (columns ভাগ করা)

```python
arr = np.array([[1, 2, 3, 4],
                [5, 6, 7, 8]])

res = np.hsplit(arr, 2)
print(res)
```

**Output:**

```
[array([[1, 2],
       [5, 6]]),
 array([[3, 4],
       [7, 8]])]
```

> কলাম অনুযায়ী ভাগ করা হয়েছে।

---

### 🔹 (C) `np.vsplit()` — Vertically Split (rows ভাগ করা)

```python
arr = np.array([[1, 2],
                [3, 4],
                [5, 6],
                [7, 8]])

res = np.vsplit(arr, 2)
print(res)
```

**Output:**

```
[array([[1, 2],
       [3, 4]]),
 array([[5, 6],
       [7, 8]])]
```

> সারি অনুযায়ী ভাগ করা হয়েছে।

---

## 📘 সংক্ষিপ্ত সারসংক্ষেপ

| ফাংশন               | কাজ                            |
| ------------------- | ------------------------------ |
| `np.concatenate()`  | একাধিক array জোড়া লাগায়        |
| `np.vstack()`       | Vertical (row-wise) stack      |
| `np.hstack()`       | Horizontal (column-wise) stack |
| `np.dstack()`       | Depth-wise (3D) stack          |
| `np.column_stack()` | Columns হিসেবে stack           |
| `np.split()`        | Array ভাগ করা                  |
| `np.hsplit()`       | Horizontally ভাগ করা           |
| `np.vsplit()`       | Vertically ভাগ করা             |

---

## ✅ মনে রাখো

* Stacking = array একত্র করা
* Splitting = array ভাগ করা
* সব array-এর shape অবশ্যই compatible হতে হবে
* এগুলো Data Preprocessing ও Reshaping-এ খুব দরকারি

# NumPy Mathematical Operations (বাংলায় উদাহরণসহ)

## 🧠 ১️⃣ Arithmetic Operators (গাণিতিক অপারেটর)

NumPy-তে প্রতিটি **operator** পুরো array-এর উপর কাজ করে — একে বলে **element-wise operation**।

---

### 🔹 উদাহরণ

```python
import numpy as np

a = np.array([10, 20, 30])
b = np.array([1, 2, 3])

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Modulus:", a % b)
print("Power:", a ** b)
```

**Output:**

```
Addition: [11 22 33]
Subtraction: [ 9 18 27]
Multiplication: [10 40 90]
Division: [10. 10. 10.]
Modulus: [0 0 0]
Power: [  10  400 27000]
```

👉 এখানে `+`, `-`, `*`, `/`, `%`, `**` সবগুলো array-এর প্রতিটি উপাদানে আলাদাভাবে প্রয়োগ হয়েছে।

---

### ⚙️ Broadcasting Concept

যদি দুইটি array-এর shape পুরোপুরি মেলে না, NumPy চেষ্টা করে **broadcasting** করে কাজটি সম্পন্ন করতে।

```python
a = np.array([[1, 2, 3],
              [4, 5, 6]])

b = np.array([10, 20, 30])

print(a + b)
```

**Output:**

```
[[11 22 33]
 [14 25 36]]
```

👉 এখানে 1D array `b` কে 2D array `a`-এর সাথে মিলিয়ে (broadcast করে) যোগ করা হয়েছে।

---

## 🔹 ২️⃣ Comparison Operators (তুলনা)

```python
a = np.array([10, 20, 30])
b = np.array([15, 20, 25])

print(a == b)
print(a > b)
print(a < b)
```

**Output:**

```
[False  True False]
[False False  True]
[ True False False]
```

👉 Boolean array রিটার্ন করে, যা Filtering বা Masking-এ ব্যবহৃত হয়।

---

# 🧮 ৩️⃣ Mathematical Functions

NumPy-তে অনেক বিল্ট-ইন গাণিতিক ফাংশন আছে, যেগুলো array-এর প্রতিটি উপাদানের উপর কাজ করে।

---

### 🔹 A. Basic Functions

```python
a = np.array([1, 4, 9, 16])

print("Square root:", np.sqrt(a))
print("Exponential:", np.exp(a))
print("Logarithm:", np.log(a))
print("Sine:", np.sin(a))
print("Cosine:", np.cos(a))
print("Tangent:", np.tan(a))
```

**Output:**

```
Square root: [1. 2. 3. 4.]
Exponential: [2.71828183 54.59815003 8103.08392758 8886110.52050787]
Logarithm: [0.         1.38629436 2.19722458 2.77258872]
Sine: [ 0.84147 -0.75680  0.41212 -0.28790]
Cosine: [ 0.54030 -0.65364 -0.91113 -0.95766]
Tangent: [ 1.55741  1.15782 -0.45232  0.30063]
```

---

### 🔹 B. Rounding & Absolute Functions

```python
a = np.array([-1.7, 2.5, 3.8, -4.2])

print("Absolute:", np.abs(a))
print("Round:", np.round(a))
print("Floor:", np.floor(a))
print("Ceil:", np.ceil(a))
```

**Output:**

```
Absolute: [1.7 2.5 3.8 4.2]
Round: [-2.  2.  4. -4.]
Floor: [-2.  2.  3. -5.]
Ceil: [-1.  3.  4. -4.]
```

---

### 🔹 C. Power, Minimum, Maximum, Sum, Product

```python
a = np.array([1, 2, 3, 4])

print("Power of 3:", np.power(a, 3))
print("Min:", np.min(a))
print("Max:", np.max(a))
print("Sum:", np.sum(a))
print("Product:", np.prod(a))
```

**Output:**

```
Power of 3: [ 1  8 27 64]
Min: 1
Max: 4
Sum: 10
Product: 24
```

---

### 🔹 D. Trigonometric & Hyperbolic Functions

```python
a = np.array([0, np.pi/2, np.pi])

print("sin:", np.sin(a))
print("cos:", np.cos(a))
print("tan:", np.tan(a))
```

**Output:**

```
sin: [0. 1. 0.]
cos: [ 1.  0. -1.]
tan: [0. 16331239353195370 0.]
```

---

## 🔹 E. Aggregate Functions

```python
arr = np.array([[1, 2, 3],
                [4, 5, 6]])

print("Sum of all:", np.sum(arr))
print("Column-wise Sum:", np.sum(arr, axis=0))
print("Row-wise Sum:", np.sum(arr, axis=1))
```

**Output:**

```
Sum of all: 21
Column-wise Sum: [5 7 9]
Row-wise Sum: [ 6 15]
```

---

## 📘 সংক্ষিপ্ত সারসংক্ষেপ

| ক্যাটেগরি     | ফাংশন / অপারেটর                                 | কাজ                                  |
| ------------- | ----------------------------------------------- | ------------------------------------ |
| Arithmetic    | `+`, `-`, `*`, `/`, `%`, `**`                   | গাণিতিক অপারেশন                      |
| Comparison    | `==`, `>`, `<`, `!=`                            | তুলনা করা                            |
| Basic Math    | `np.sqrt()`, `np.exp()`, `np.log()`             | মৌলিক গণিত                           |
| Trigonometric | `np.sin()`, `np.cos()`, `np.tan()`              | ত্রিকোণমিতি                          |
| Rounding      | `np.round()`, `np.floor()`, `np.ceil()`         | মান গোল করা                          |
| Aggregate     | `np.sum()`, `np.min()`, `np.max()`, `np.prod()` | সারি / কলাম অনুযায়ী যোগ, গুণ ইত্যাদি |

---

## ✅ সারসংক্ষেপে মনে রাখো

* NumPy সব গাণিতিক কাজ **element-wise** করে
* Broadcasting-এর মাধ্যমে ভিন্ন shape-এর array-এর উপরও অপারেশন সম্ভব
* Mathematical functions খুব দ্রুত এবং C-level optimized
* Aggregate ফাংশন দিয়ে সহজেই সারি/কলাম ভিত্তিক বিশ্লেষণ করা যায়

