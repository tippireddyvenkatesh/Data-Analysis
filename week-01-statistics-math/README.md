# Week 1 – Statistics & Basic Math

## ✅ Topics Covered
- Mean, Median, Mode
- Standard Deviation & Variance
- Normal Distribution
- Percentiles & Quartiles
- Probability Basics
- Basic Arithmetic
- Weighted Average
- Cumulative Sum

## 📘 What I Learned
- How central tendency helps summarize data
- The importance of standard deviation in measuring spread
- What makes data "normally distributed" and why it matters
- How to use percentiles and quartiles to detect outliers
- The power of cumulative sum in trend analysis

## 🔧 Tools Used
- Pen & paper for understanding math logic
- Excel (for calculating mean, median, SD)

## 🧠 Insights
- Standard Deviation is relative — you need context!
- Normal distribution is assumed in many models but doesn't apply to all datasets
- Probability basics are simple but extremely useful in real-world analytics

## 🔗 Helpful Resources
- [Simplilearn - Statistics Tutorial](https://www.simplilearn.com/tutorials/statistics-tutorial)
- [LunarTech Statistics Guide](https://news.lunartech.ai/fundamentals-of-statistics-for-data-scientists-and-data-analysts-69d93a05aae7)

---

## 💻 Examples & Code Snippets

### 📌 Mean, Median, Mode

**Example Data:** `[10, 20, 20, 30, 40]`

- **Mean:**  
  \[
  \text{Mean} = \frac{10 + 20 + 20 + 30 + 40}{5} = 24
  \]

- **Median:**  
  Sorted data = `[10, 20, 20, 30, 40]`  
  Middle value = **20**

- **Mode:**  
  Most frequent = **20**

---

### 📌 Standard Deviation & Variance

**Data:** `[10, 20, 30, 40, 50]`

- **Mean:** 30  
- **Variance:**  
  \[
  \frac{(10-30)^2 + (20-30)^2 + ...}{5} = 200
  \]

- **Standard Deviation:**  
  \[
  \sqrt{200} ≈ 14.14
  \]

**Python Snippet:**
```python
import statistics
data = [10, 20, 30, 40, 50]
print("SD:", statistics.stdev(data))
```

---

### 📌 Normal Distribution

- **Example:** Exam scores of 1,000 students usually follow a bell curve.
- In a perfect normal distribution:
  - Mean = Median = Mode
  - 68% of data lies within 1 standard deviation
  - 95% within 2 SDs
  - 99.7% within 3 SDs

---

### 📌 Percentiles & Quartiles

**Data:** `[10, 20, 30, 40, 50, 60, 70, 80]`

- **Q1 (25th percentile):** 20  
- **Q2 (Median / 50th):** 40  
- **Q3 (75th percentile):** 60  

**IQR (Interquartile Range):**  
\[
IQR = Q3 - Q1 = 60 - 20 = 40
\]

---

### 📌 Probability Basics

**Example:** What’s the probability of rolling an even number on a die?

- Even outcomes = 2, 4, 6 → 3 outcomes  
- Total outcomes = 6  

\[
P = \frac{3}{6} = 0.5 = 50\%
\]

---

### 📌 Basic Arithmetic

**Example:**
- Addition: `10 + 5 = 15`
- Subtraction: `10 - 5 = 5`
- Multiplication: `10 * 5 = 50`
- Division: `10 / 2 = 5`

**Order of Operations Example:**
```python
result = 2 + 3 * 4  # Output: 14 (not 20)
```

---

### 📌 Weighted Average

**Example:**

- Math = 90 (weight: 4)  
- English = 80 (weight: 2)  

\[
\text{Weighted Avg} = \frac{(90×4) + (80×2)}{6} = \frac{520}{6} ≈ 86.67
\]

---

### 📌 Cumulative Sum

**Data:** `[10, 20, 30, 40]`  
**Running total:** `[10, 30, 60, 100]`

**Python Snippet:**
```python
import itertools
data = [10, 20, 30, 40]
print(list(itertools.accumulate(data)))
```
