
---

# 📘 **MODULE 1: FOUNDATIONS (Full Detailed Guide)**

This module has **4 chapters**, and I’m giving you the complete guide right here.

---

# --------------------------------------

# **CHAPTER 1: What is DSA & Why Learn It?**

# --------------------------------------

## ✅ **What is DSA?**

**Data Structures** → How we store data
**Algorithms** → How we process data

### Examples:

* Arrays → store items in order
* Hash tables → store key/value pairs
* Graphs → store networks
* Sorting algorithms → sort data efficiently
* Searching algorithms → find data efficiently

---

## ✅ **Why DSA matters (especially in JavaScript)?**

* Improves problem-solving
* Helps you write fast & optimized code
* Needed for **interviews** (FAANG, remote jobs)
* Used in **backend**, **frontend**, **APIs**, **systems**

### Real-world examples:

* Instagram feed → graph + priority queue
* Google search suggestions → trie
* WhatsApp contact search → hashing
* Netflix streaming → dynamic programming

---

## ✅ **Where JS is used in DSA?**

* Web development
* Full-stack systems
* Competitive programming
* Browser APIs
* Node.js backend systems

---

## 🧠 **Summary**

Learning DSA = building a “brain” for solving any problem.

---

# --------------------------------------

# **CHAPTER 2: Time & Space Complexity (Big-O)**

# --------------------------------------

## ✅ **Why learn Big-O?**

Because without it, you can’t measure if your algorithm is:

* fast
* scalable
* optimized

---

## 📌 **Common Time Complexities**

| Complexity | Meaning          | Example         |
| ---------- | ---------------- | --------------- |
| O(1)       | Constant         | Hash lookup     |
| O(log n)   | Logarithmic      | Binary search   |
| O(n)       | Linear           | Loop            |
| O(n log n) | Divide & Conquer | Merge sort      |
| O(n²)      | Quadratic        | Nested loops    |
| O(2ⁿ)      | Exponential      | Recursion (bad) |
| O(n!)      | Factorial        | Permutations    |

---

## 📌 **Examples in JavaScript**

### **O(n) Example**

```js
function sum(arr) {
  let total = 0;
  for (let num of arr) total += num;
  return total;
}
```

### **O(n²) Example**

```js
for (let i = 0; i < n; i++) {
  for (let j = 0; j < n; j++) {
    console.log(i, j);
  }
}
```

### **O(log n) Example**

```js
function binarySearch(arr, target) {
  let left = 0;
  let right = arr.length - 1;

  while (left <= right) {
    let mid = Math.floor((left + right) / 2);

    if (arr[mid] === target) return mid;
    if (arr[mid] < target) left = mid + 1;
    else right = mid - 1;
  }

  return -1;
}
```

---

## 🧠 **Summary**

Big-O tells you *how much time and memory* your code needs as input grows.

---

# --------------------------------------

# **CHAPTER 3: Math for DSA**

# --------------------------------------

## 🔢 1. Logarithms (Very Important)

You’ll see `log` in:

* binary search
* heap
* quicksort
* mergesort

### Example:

`log₂ 8 = 3` (because 2³ = 8)

---

## 🔢 2. GCD & LCM

Used in:

* number theory
* cryptography
* math DP problems

### Example: GCD using Euclid’s Algorithm (O(log n))

```js
function gcd(a, b) {
  return b === 0 ? a : gcd(b, a % b);
}
```

---

## 🔢 3. Prime Numbers + Sieve of Eratosthenes

Used in:

* hashing
* cryptography
* probability

### Sieve Example

```js
function sieve(n) {
  const isPrime = new Array(n + 1).fill(true);
  isPrime[0] = isPrime[1] = false;

  for (let i = 2; i * i <= n; i++) {
    if (isPrime[i]) {
      for (let j = i * i; j <= n; j += i) {
        isPrime[j] = false;
      }
    }
  }
  return isPrime;
}
```

---

# --------------------------------------

# **CHAPTER 4: JavaScript Essentials for DSA**

# --------------------------------------

You must master these before moving forward.

---

## 🔥 1. Arrays & Methods

* push
* pop
* shift
* unshift
* slice
* splice
* map
* filter
* reduce

---

## 🔥 2. Objects + Maps + Sets

### Map Example

```js
const mp = new Map();
mp.set("x", 10);
mp.set("y", 20);
```

### Set Example

```js
const st = new Set([1, 2, 3, 3]);
console.log(st); // {1, 2, 3}
```

---

## 🔥 3. Recursion (Core for DSA)

```js
function factorial(n) {
  if (n === 1) return 1;
  return n * factorial(n - 1);
}
```

---

## 🔥 4. Classes (Useful for Linked Lists, Trees)

```js
class Node {
  constructor(value) {
    this.value = value;
    this.next = null;
  }
}
```

---

## 🔥 5. ES6 features needed for DSA

* let, const
* arrow functions
* spread operator
* rest operator
* destructuring

---
