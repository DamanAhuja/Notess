# Adv Algo
# 📘 **UNIT 1 — List & Iterator ADTs**

**Topics Covered:**

* Abstract Data Types (ADT)
* Vectors
* Lists
* Sequences
* Iterators
  *(4 Hours – But extremely foundational for all later units)*

---

## 🔹 1. ABSTRACT DATA TYPE (ADT)

### ✅ Definition

An **Abstract Data Type (ADT)** is a *logical description of a data structure*, focusing on:

* What operations can be performed
* NOT how they are implemented

👉 It hides the internal representation and shows only behavior.

---

### ✅ ADT vs Data Structure

| ADT             | Data Structure                 |
| --------------- | ------------------------------ |
| Logical concept | Physical implementation        |
| What operations | How operations are implemented |
| Example: List   | Example: Array, Linked List    |

---

### ✅ Example of List ADT (Conceptual)

Operations:

* insert(x)
* delete(pos)
* search(x)
* size()
* isEmpty()

Implementation can be:

* Array List
* Linked List

---

✅ **Exam Line:**

> ADT provides data abstraction and separates the user’s view from the implementation.

---

## 🔹 2. VECTOR ADT

### ✅ Definition

A **Vector** is a **dynamic array** that:

* Stores elements in **contiguous memory**
* Automatically **resizes**
* Supports **random access**

---

### ✅ Core Operations

| Operation    | Description               | Time Complexity |
| ------------ | ------------------------- | --------------- |
| at(i)        | Access element at index i | O(1)            |
| insert(i, x) | Insert at index           | O(n)            |
| push_back(x) | Add at end                | O(1) amortized  |
| pop_back()   | Remove last element       | O(1)            |
| size()       | Number of elements        | O(1)            |
| capacity()   | Allocated memory          | O(1)            |

---

### ✅ Dynamic Resizing Concept

When capacity is full:

1. New array of **double size**
2. Copy all elements
3. Old array deleted

✅ This is why insertion at end is **amortized O(1)** not worst-case.

---

### ✅ Advantages

✔ Fast access
✔ Cache friendly
✔ Easy to implement

### ✅ Disadvantages

❌ Slow insertion/deletion in middle
❌ Memory wastage due to unused capacity

---

## 🔹 3. LIST ADT

### ✅ Definition

A **List** is a **linear collection of elements** where:

* Elements have a **position**
* Access is generally **sequential**

---

### ✅ List ADT Operations

| Operation    | Meaning                |
| ------------ | ---------------------- |
| insert(i, x) | Insert at position i   |
| remove(i)    | Remove from position i |
| get(i)       | Get element at i       |
| find(x)      | Search element         |
| isEmpty()    | Check if empty         |
| size()       | Count elements         |

---

## 🔹 4. TYPES OF LIST IMPLEMENTATION

---

### ✅ (A) ARRAY LIST

* Stored in contiguous memory
* Fixed size or dynamic array

| Operation     | Time |
| ------------- | ---- |
| Access        | O(1) |
| Insert/Delete | O(n) |
| Search        | O(n) |

✅ Used when:

* Fast access needed
* Insertions are less frequent

---

### ✅ (B) LINKED LIST

Each node has:

* Data
* Next pointer

Types:

* Singly Linked List
* Doubly Linked List
* Circular Linked List

---

#### ✅ Singly Linked List Node

```
[Data | Next]
```

| Operation           | Time |
| ------------------- | ---- |
| Insert at beginning | O(1) |
| Delete at beginning | O(1) |
| Search              | O(n) |
| Access by index     | O(n) |

---

### ✅ Comparison: Array List vs Linked List

| Feature        | Array List | Linked List    |
| -------------- | ---------- | -------------- |
| Memory         | Contiguous | Non-contiguous |
| Access         | O(1)       | O(n)           |
| Insert/Delete  | O(n)       | O(1)           |
| Cache Friendly | Yes        | No             |

---

## 🔹 5. SEQUENCE ADT

### ✅ Definition

A **Sequence** is a **generalization of vector + list**, supporting:

* Element access by index
* Insertion & deletion
* Iterator traversal

👉 It combines features of both vector and list.

---

### ✅ Operations

* at(i)
* insert(i, x)
* erase(i)
* begin()
* end()
* size()

---

✅ Implemented using:

* Arrays
* Linked Lists
* Deques

---

## 🔹 6. ITERATOR ADT (VERY IMPORTANT FOR EXAMS 🔥)

### ✅ Definition

An **Iterator** is an object that:

* Points to an element in a container
* Allows traversal without exposing internal structure

---

### ✅ Why Iterators Are Needed?

✔ Uniform traversal
✔ Data structure independence
✔ Works for all containers
✔ Safer than raw pointers

---

### ✅ Basic Iterator Operations

| Operation  | Meaning            |
| ---------- | ------------------ |
| begin()    | First element      |
| end()      | After last element |
| ++it       | Move forward       |
| *it        | Access value       |
| it1 == it2 | Compare            |

---

### ✅ Example Concept (C++ Style)

```
for(it = v.begin(); it != v.end(); it++) {
    print(*it);
}
```

---

### ✅ Types of Iterators (Theoretical)

| Type          | Movement           |
| ------------- | ------------------ |
| Input         | Read only, forward |
| Output        | Write only         |
| Forward       | Read + Write       |
| Bidirectional | Forward + Backward |
| Random Access | Jump anywhere      |

---

## 🔹 7. RELATION BETWEEN VECTOR, LIST, SEQUENCE & ITERATOR

| Structure | Supports Random Access | Uses Iterator |
| --------- | ---------------------- | ------------- |
| Vector    | ✅ Yes                  | ✅ Yes         |
| List      | ❌ No                   | ✅ Yes         |
| Sequence  | ✅ Yes                  | ✅ Yes         |

---

## 🔹 8. APPLICATIONS (VERY IMPORTANT FOR LONG ANSWERS)

* Vectors → Dynamic memory, graphics, simulations
* Lists → Undo operations, browser history
* Sequences → Text editors, playlists
* Iterators → STL traversal, databases

---

## 🔹 9. COMMON EXAM QUESTIONS FROM UNIT 1

### ✅ 2 Marks:

* Define ADT
* What is a Vector?
* Define Iterator
* What is a List?

---

### ✅ 5 Marks:

* Compare Vector and List
* Explain Dynamic Resizing in Vector
* Explain Sequence ADT
* Advantages of Iterators

---

### ✅ 10 Marks:

* Explain List ADT and its implementations in detail
* Explain Vector ADT with operations and complexity
* Write detailed notes on Iterator ADT

---

# 📘 **UNIT 2 — HASH TABLES & DICTIONARIES**

**Topics Covered:**

* Dictionaries
* Hash Tables
* Hash Functions
* Collision Resolution Techniques
  *(6 Hours – VERY important & scoring unit)*

---

## 🔹 1. DICTIONARY ADT

### ✅ Definition

A **Dictionary (or Map)** is an ADT that stores **(key, value)** pairs such that:

* Each **key is unique**
* Each key maps to exactly one value

---

### ✅ Dictionary Operations

| Operation    | Meaning                 |
| ------------ | ----------------------- |
| insert(k, v) | Insert key-value pair   |
| remove(k)    | Delete entry with key k |
| search(k)    | Return value of key k   |
| size()       | Number of entries       |
| isEmpty()    | Check if empty          |

---

### ✅ Real-Life Examples

* Roll number → Student name
* Account number → Balance
* Word → Meaning

---

✅ **Exam Line:**

> A dictionary is a dynamic set supported with insertion, deletion and search based on keys.

---

## 🔹 2. NEED FOR HASH TABLES

Traditional Searching:

* Array → O(n)
* Linked List → O(n)
* Binary Search → O(log n) *(requires sorted data)*

✅ **Hash Table provides average O(1) time** for:

* Insertion
* Deletion
* Searching

That’s why it is widely used in:

* Databases
* Compilers
* Password storage
* Caches

---

## 🔹 3. HASH TABLE — DEFINITION

### ✅ Definition

A **Hash Table** is a data structure that:

* Uses a **hash function** to map keys to array indices
* Stores elements at computed positions

```
Index = h(key)
```

---

### ✅ Structure of Hash Table

| Component     | Description                |
| ------------- | -------------------------- |
| Key           | Input value                |
| Hash Function | Converts key → index       |
| Table         | Array where data is stored |

---

## 🔹 4. HASH FUNCTION (VERY IMPORTANT 🔥)

### ✅ Definition

A **Hash Function** is a function that maps a key into a table index.

```
h(k) → {0, 1, 2, ..., m-1}
```

where `m = table size`

---

### ✅ Properties of a Good Hash Function

✔ Uniform distribution
✔ Fast computation
✔ Minimum collisions
✔ Deterministic (same key → same index)

---

### ✅ Types of Hash Functions

---

### 1️⃣ Division Method

```
h(k) = k mod m
```

✅ Most commonly used
✅ Choose `m` as a prime number

---

### 2️⃣ Mid-Square Method

* Square the key
* Extract middle digits

✅ More uniform distribution

---

### 3️⃣ Multiplication Method

```
h(k) = ⌊ m (kA mod 1) ⌋
```

where `0 < A < 1`

✅ Less clustering

---

### 4️⃣ Folding Method

* Split key into parts
* Add them together

✅ Used for large numeric keys

---

## 🔹 5. COLLISION — HEART OF UNIT 2 🔥

### ✅ Definition

A **collision occurs when two different keys map to the same index**.

```
h(k1) = h(k2)
```

---

### ✅ Why Collisions Occur?

* Limited table size
* Poor hash function
* Large number of keys

---

## 🔹 6. COLLISION RESOLUTION TECHNIQUES

---

# ✅ (A) SEPARATE CHAINING

### ✅ Concept

Each table index stores a **linked list of elements**.

```
Table[5] → [key1 → key2 → key3]
```

---

### ✅ Operations & Complexity

| Operation | Average | Worst |
| --------- | ------- | ----- |
| Insert    | O(1)    | O(n)  |
| Search    | O(1)    | O(n)  |
| Delete    | O(1)    | O(n)  |

---

### ✅ Advantages

✔ Simple
✔ No overflow problem
✔ Easy deletion

### ✅ Disadvantages

❌ Extra memory for pointers
❌ Poor cache utilization

---

# ✅ (B) OPEN ADDRESSING

All elements are stored **inside the hash table itself**.

If collision occurs → find another empty slot.

---

## 🔹 1. Linear Probing

```
h(k, i) = (h(k) + i) mod m
```

Try one by one next slot.

---

### ✅ Problem: Primary Clustering

Consecutive occupied slots form large clusters.

---

## 🔹 2. Quadratic Probing

```
h(k, i) = (h(k) + i²) mod m
```

Reduces clustering.

---

## 🔹 3. Double Hashing

```
h(k, i) = (h1(k) + i*h2(k)) mod m
```

✅ Best probing technique
✅ Least clustering

---

## 🔹 7. LOAD FACTOR (α) — VERY IMPORTANT EXAM TERM

### ✅ Definition

```
α = n / m
```

where

* `n` = number of keys
* `m` = table size

---

### ✅ Effect of Load Factor

| α Value | Performance     |
| ------- | --------------- |
| Small   | Faster          |
| Large   | More collisions |

---

✅ In Open Addressing:

```
α < 0.7 is recommended
```

---

## 🔹 8. REHASHING

### ✅ Definition

When load factor becomes too large:

1. Create a **new table with double size**
2. Reinsert all keys using new hash function

✅ Improves performance

---

## 🔹 9. COMPARISON OF COLLISION TECHNIQUES

| Feature     | Chaining | Open Addressing |
| ----------- | -------- | --------------- |
| Memory      | More     | Less            |
| Deletion    | Easy     | Difficult       |
| Performance | Stable   | Depends on α    |
| Overflow    | Never    | Possible        |

---

## 🔹 10. APPLICATIONS OF HASH TABLES

* Password Authentication
* Symbol Tables in Compilers
* Database Indexing
* Caching
* Blockchain
* Networks

---

## 🔹 11. TIME COMPLEXITY SUMMARY

| Operation | Average | Worst |
| --------- | ------- | ----- |
| Insert    | O(1)    | O(n)  |
| Search    | O(1)    | O(n)  |
| Delete    | O(1)    | O(n)  |

---

## 🔹 12. COMMON EXAM QUESTIONS (VERY PREDICTABLE ✅)

### ✅ 2 Marks:

* Define Hash Table
* What is Collision?
* Define Load Factor
* What is a Dictionary?

---

### ✅ 5 Marks:

* Explain Hash Function
* Explain Collision Resolution
* Explain Chaining
* Explain Linear Probing
* What is Rehashing?

---

### ✅ 10 Marks:

* Explain Hash Tables with all collision techniques
* Compare Chaining and Open Addressing
* Explain Open Addressing methods in detail
* Explain Hash Function and its properties

---


# 📕 **UNIT 3 — STRINGS & TRIES (8 HOURS)**

### ✅ Topics Covered:

* String Basics
* String Matching
* **KMP Algorithm**
* Tries

  * Standard Tries
  * Compressed Tries
  * **Suffix Tries**
* Applications in **Search Engines**

---

# 🔹 1. STRING — BASIC CONCEPT

### ✅ Definition

A **String** is a sequence of characters taken from a finite alphabet.

Example:

```
"algorithm", "data", "school"
```

---

### ✅ String Operations

| Operation        | Purpose                        |
| ---------------- | ------------------------------ |
| Length           | Total characters               |
| Compare          | Lexicographic comparison       |
| Substring        | Extract part                   |
| Concatenate      | Join two strings               |
| Pattern Matching | Find one string inside another |

---

✅ **Core Problem in this Unit:**

> Efficient **Pattern Searching in a Text**

---

# 🔹 2. STRING MATCHING PROBLEM

### ✅ Definition

Given:

* **Text T** of length `n`
* **Pattern P** of length `m`

Find all positions where `P` occurs in `T`.

Example:

```
T = ABABDABACDABABCABAB
P = ABABCABAB
```

---

## ❌ Naive String Matching Algorithm

### ✅ Idea

Match pattern at every position of text.

### ✅ Time Complexity

```
O(n × m)   ❌ (Very slow for large data)
```

---

✅ This inefficiency leads to the development of **KMP Algorithm** ✅

---

# 🔥 3. KMP (KNUTH–MORRIS–PRATT) ALGORITHM — VERY IMPORTANT 🔥🔥🔥

### ✅ Purpose

To avoid unnecessary comparisons while matching the pattern.

✅ It uses a **preprocessed table (LPS array)**.

---

## ✅ Key Idea of KMP

When a mismatch occurs:

* Do **NOT restart from beginning of pattern**
* Shift pattern using **LPS array**

---

## 🔹 3.1 LPS ARRAY (Longest Prefix Suffix)

### ✅ Definition

For each index `i` in pattern:

```
LPS[i] = length of longest proper prefix
         which is also a suffix
```

---

### ✅ Example

Pattern:

```
A B A B C A B A B
0 1 2 3 4 5 6 7 8
```

LPS Array:

```
0 0 1 2 0 1 2 3 4
```

---

### ✅ How LPS Helps?

It tells:

> "How many characters we can safely skip after mismatch"

---

## 🔹 3.2 KMP ALGORITHM STEPS

### ✅ Step 1: Build LPS Array

Time: `O(m)`

### ✅ Step 2: Match Pattern with Text

Time: `O(n)`

---

### ✅ Total Time Complexity

```
O(n + m) ✅✅✅
```

---

## 🔹 3.3 KMP DRY RUN (Exam Favorite 🔥)

Text:

```
ABABDABACDABABCABAB
```

Pattern:

```
ABABCABAB
```

1. Precompute LPS
2. Match character by character
3. On mismatch → jump using LPS
4. Pattern found at correct index

✅ **Examiner checks your understanding using this dry run**

---

## ✅ KMP SUMMARY

| Feature         | Value                                 |
| --------------- | ------------------------------------- |
| Preprocessing   | Yes                                   |
| Time Complexity | O(n+m)                                |
| Extra Space     | O(m)                                  |
| Applications    | Text search, Plagiarism, DNA matching |

---

# 🔹 4. TRIE DATA STRUCTURE (VERY VERY IMPORTANT 🔥)

---

## ✅ Definition

A **Trie (Prefix Tree)** is a tree-based data structure used to store **strings efficiently**.

Each node:

* Represents a **character**
* Paths represent **words**

---

### ✅ Example Words:

```
cat, car, cap
```

```
        (root)
        /   \
       c
       |
       a
     /  |  \
    t   r   p
```

---

## 🔹 4.1 TRIE OPERATIONS

| Operation | Time |
| --------- | ---- |
| Insert    | O(L) |
| Search    | O(L) |
| Delete    | O(L) |

where `L = length of word`

---

## 🔹 4.2 INSERT OPERATION IN TRIE

* Start from root
* For each character:

  * If exists → move forward
  * Else → create node

---

## 🔹 4.3 SEARCH OPERATION IN TRIE

* Traverse character by character
* If any character missing → word not present

---

## ✅ Advantages of Trie

✔ Fast searching
✔ No collisions
✔ Ideal for prefix searching
✔ Works better than hash tables for strings

---

## ❌ Disadvantages

❌ High memory usage
❌ Not cache friendly

---

# 🔹 5. COMPRESSED TRIE (PATTERN TRIE)

### ✅ Definition

A **Compressed Trie** removes unnecessary single-child chains by compressing edges.

---

### ✅ Benefit

✔ Saves memory
✔ Faster traversal
✔ Used in large dictionary systems

---

# 🔥 6. SUFFIX TRIE (VERY IMPORTANT 🔥🔥🔥)

---

## ✅ Definition

A **Suffix Trie** is a Trie that stores **all suffixes of a string**.

---

### ✅ Example

String:

```
BANANA
```

Suffixes:

```
BANANA  
ANANA  
NANA  
ANA  
NA  
A
```

All inserted into a Trie ✅

---

## ✅ Applications of Suffix Trie

| Application                | Use  |
| -------------------------- | ---- |
| Pattern searching          | O(m) |
| Longest repeated substring | Yes  |
| DNA sequence matching      | Yes  |
| Plagiarism detection       | Yes  |

---

## ✅ Time & Space Complexity

| Feature      | Value |
| ------------ | ----- |
| Construction | O(n²) |
| Search       | O(m)  |
| Space        | O(n²) |

---

# 🔹 7. TRIE vs HASH TABLE (VERY COMMON EXAM QUESTION ✅)

| Feature       | Trie  | Hash Table |
| ------------- | ----- | ---------- |
| Prefix Search | ✅ Yes | ❌ No       |
| Speed         | O(L)  | O(1)       |
| Memory        | High  | Low        |
| Collision     | No    | Yes        |

---

# 🔹 8. ROLE OF TRIES IN SEARCH ENGINES

---

## ✅ Search Engine Tasks

* Auto-suggest
* Auto-complete
* Spell check
* Keyword matching
* Fast lookup

✅ All powered using:

* **Tries**
* **Compressed Tries**
* **Suffix Tries**

---

### ✅ Example:

Typing:

```
"go"
```

Suggestions:

```
google, good, govt, gold
```

---

# 🔹 9. APPLICATIONS OF STRING MATCHING & TRIES

* Google Search
* DNA Matching
* Plagiarism Detection
* Compiler token matching
* Spam Detection
* Pattern Recognition

---

# 🔹 10. COMPLETE TIME COMPLEXITY SUMMARY

| Algorithm         | Time   |
| ----------------- | ------ |
| Naive Matching    | O(nm)  |
| KMP               | O(n+m) |
| Trie Insert       | O(L)   |
| Trie Search       | O(L)   |
| Suffix Trie Build | O(n²)  |

---

# 🔹 11. MOST IMPORTANT EXAM QUESTIONS ✅✅✅

---

## ✅ 2 Marks

* Define String Matching
* What is LPS?
* What is a Trie?
* Define Suffix Trie

---

## ✅ 5 Marks

* Explain KMP Algorithm
* Explain Trie with example
* Applications of Trie
* Difference between Trie & Hash Table

---

## ✅ 10 Marks (VERY HIGH PROBABILITY 🔥)

1. Explain **KMP Algorithm with example and dry run**
2. Explain **Trie Data Structure with operations**
3. Explain **Suffix Trie with construction**
4. Role of **Trie in Search Engines**

---

# 📘 **UNIT 4 — MORE ON TREES (8 HOURS)**

### ✅ Topics Covered:

* **2–4 Trees (also called 2–3–4 Trees)**
* **B-Trees**

These trees are the **foundation of database indexing, file systems, and large-scale storage systems**.

---

# 🔹 1. WHY DO WE NEED ADVANCED TREES?

### ❌ Problems with Binary Search Trees (BST)

* Can become **skewed**
* Worst-case time = **O(n)**
* Not suitable for **disk-based storage**

---

### ✅ Solution → Self-Balancing Multiway Trees

* **2–4 Trees**
* **B-Trees**

✔ Always balanced
✔ Height is kept minimum
✔ Guaranteed **O(log n)** operations

---

# 🔥 2. 2–4 TREE (2–3–4 TREE)

---

## ✅ Definition

A **2–4 Tree** is a **self-balancing multiway search tree** in which each node can have:

| Node Type | Keys   | Children   |
| --------- | ------ | ---------- |
| 2-node    | 1 key  | 2 children |
| 3-node    | 2 keys | 3 children |
| 4-node    | 3 keys | 4 children |

---

### ✅ Properties of 2–4 Tree

1. All leaves are at the **same level** ✅
2. Each node can have **1 to 3 keys**
3. Each internal node can have **2 to 4 children**
4. It is always **perfectly height-balanced**
5. Keys inside a node are always in **sorted order**

---

## 🔹 2.1 SEARCH IN 2–4 TREE

### ✅ Steps:

1. Compare key with node keys
2. Move to correct child
3. Repeat until found or reach leaf

---

### ✅ Time Complexity:

```
O(log n)
```

---

## 🔹 2.2 INSERTION IN 2–4 TREE (VERY IMPORTANT 🔥)

### ✅ Basic Idea

* Always insert at a **leaf node**
* If leaf becomes **overflow (4 keys)** → split it

---

### ✅ Splitting a 4-Node

If a node has:

```
[a | b | c]
```

After inserting new key → overflow (4 keys)

Steps:

1. Middle key **b moves up**
2. Left key goes to **left child**
3. Right key goes to **right child**

✅ Tree remains balanced

---

### ✅ Special Case: Root Split

If **root splits**, a new root is created → **tree height increases by 1**

---

### ✅ Insertion Time:

```
O(log n)
```

---

## 🔹 2.3 DELETION IN 2–4 TREE (THEORY LEVEL)

Deletion is done carefully to:

* Avoid **node having 0 keys**
* Borrow from sibling or
* Merge nodes when required

✅ Still remains balanced
✅ Time complexity: **O(log n)**

---

## 🔹 2.4 ADVANTAGES OF 2–4 TREES

✔ Always balanced
✔ Guaranteed log time for search, insert, delete
✔ Used as the **basis of Red-Black Trees**
✔ Better than BST for large datasets

---

## 🔹 2.5 DISADVANTAGES

❌ Complex implementation
❌ Not directly used in databases
❌ High memory overhead

---

# 🔥 3. B-TREE (MOST IMPORTANT TREE FOR EXAMS 🔥🔥🔥)

---

## ✅ Definition

A **B-Tree** is a **generalized, self-balancing m-ary search tree** designed for **disk storage and databases**.

---

## ✅ Order of B-Tree (m)

A B-Tree of order **m** means:

| Property                | Rule           |
| ----------------------- | -------------- |
| Max children            | m              |
| Max keys                | m − 1          |
| Min children (non-root) | ⌈m/2⌉          |
| Min keys                | ⌈m/2⌉ − 1      |
| Root special case       | Can have fewer |

---

## 🔹 3.1 PROPERTIES OF B-TREE (EXAM DEFINITIONS ✅)

1. All leaves appear at the **same level**
2. Keys in a node are in **sorted order**
3. Every node has **at most (m−1) keys**
4. Every internal node has **at most m children**
5. Except root, every node has **at least ⌈m/2⌉ children**
6. Height of B-Tree is always **O(log n)**

---

# 🔹 3.2 SEARCH IN B-TREE

### ✅ Steps:

1. Start from root
2. Perform **binary search within node**
3. Move to correct child
4. Repeat until found or leaf reached

---

### ✅ Time Complexity:

```
O(log n)
```

---

# 🔥 3.3 INSERTION IN B-TREE (VERY HIGH PROBABILITY 🔥)

---

### ✅ Step 1: Insert Like BST

* Find correct leaf
* Insert in sorted order

---

### ✅ Step 2: Handle Overflow

If node gets **m keys → overflow**

✅ Split the node:

* Middle key moves up
* Left part → left child
* Right part → right child

---

### ✅ Root Split Case

If root overflows:

* Create a **new root**
* Increase height by 1

---

### ✅ Insertion Complexity:

```
O(log n)
```

---

# 🔥 3.4 DELETION IN B-TREE (IMPORTANT THEORY)

---

### ✅ Three Cases of Deletion

---

### ✅ Case 1: Key in Leaf Node

* Simply delete
* If underflow occurs → borrow or merge

---

### ✅ Case 2: Key in Internal Node

* Replace with:

  * Inorder predecessor OR
  * Inorder successor
* Then delete that key from leaf

---

### ✅ Case 3: Underflow Handling

If node has **less than minimum keys**:

* **Borrow from sibling**
* OR **Merge with sibling**

---

### ✅ Deletion Complexity:

```
O(log n)
```

---

# 🔹 4. B-TREE vs 2–4 TREE (VERY COMMON EXAM QUESTION ✅)

| Feature      | 2–4 Tree     | B-Tree       |
| ------------ | ------------ | ------------ |
| Type         | Special case | General case |
| Max children | 4            | m            |
| Disk usage   | No           | ✅ Yes        |
| Used in DB   | ❌ No         | ✅ Yes        |
| Height       | Logarithmic  | Logarithmic  |

✅ **2–4 tree is a special case of B-Tree where m = 4**

---

# 🔹 5. B-TREE vs BINARY SEARCH TREE ✅

| Feature     | BST            | B-Tree          |
| ----------- | -------------- | --------------- |
| Balance     | Not guaranteed | Always balanced |
| Height      | O(n) worst     | O(log n)        |
| Disk access | Poor           | Excellent       |
| Use in DB   | ❌ No           | ✅ Yes           |

---

# 🔹 6. APPLICATIONS OF B-TREES

🔥 Very Important for exams

* Database indexing (MySQL, Oracle)
* File systems (NTFS, ext4)
* Large block storage
* Operating systems
* Data warehouses

---

# 🔹 7. TIME COMPLEXITY SUMMARY

| Operation | 2–4 Tree | B-Tree   |
| --------- | -------- | -------- |
| Search    | O(log n) | O(log n) |
| Insert    | O(log n) | O(log n) |
| Delete    | O(log n) | O(log n) |

---

# 🔹 8. MOST IMPORTANT EXAM QUESTIONS ✅✅✅

---

### ✅ 2 Marks

* Define 2–4 Tree
* Define B-Tree
* What is order of B-Tree?

---

### ✅ 5 Marks

* Properties of 2–4 Tree
* Advantages of B-Tree
* Compare BST and B-Tree
* Applications of B-Tree

---

### ✅ 10 Marks (🔥 Guaranteed)

1. Explain **2–4 Tree with insertion and properties**
2. Explain **B-Tree with insertion and deletion**
3. Compare **2–4 Tree and B-Tree**
4. Explain **Applications of B-Tree in databases**

---

# 📘 **UNIT 5 — ADVANCED GRAPHS (8 HOURS)**

### ✅ Topics Covered:

* Graph Basics (Quick Revision)
* **Bellman–Ford Algorithm**
* **Union–Find Data Structure**
* **Kruskal’s Algorithm**
* Applications & Complexity

---

# 🔹 1. GRAPH — QUICK FOUNDATION (EXAM REVISION)

---

## ✅ Definition

A **Graph G** is defined as:

```
G = (V, E)
```

where

* `V` = set of vertices (nodes)
* `E` = set of edges (connections)

---

## ✅ Types of Graphs

| Type               | Description             |
| ------------------ | ----------------------- |
| Undirected         | Edges have no direction |
| Directed (Digraph) | Edges have direction    |
| Weighted           | Edges have weights      |
| Unweighted         | All edges equal         |

---

## ✅ Graph Representations

### 1️⃣ Adjacency Matrix

* Space: `O(V²)`
* Fast lookup

### 2️⃣ Adjacency List

* Space: `O(V + E)`
* Used in most algorithms ✅

---

# 🔥 2. BELLMAN–FORD ALGORITHM (VERY IMPORTANT)

---

## ✅ Purpose

Find the **shortest path from a single source to all other vertices**
✅ Works with **negative edge weights**
❌ Detects **negative weight cycles**

---

## ✅ Difference from Dijkstra

| Feature          | Dijkstra   | Bellman-Ford |
| ---------------- | ---------- | ------------ |
| Negative weights | ❌ No       | ✅ Yes        |
| Time complexity  | O(E log V) | O(VE)        |
| Cycle detection  | ❌ No       | ✅ Yes        |

---

## 🔹 2.1 PRINCIPLE OF BELLMAN–FORD

* Relax all edges **(V − 1) times**
* Because max edges in shortest path = `V − 1`

---

## 🔹 2.2 RELAXATION PROCESS

For each edge `(u, v)` with weight `w`:

```
if dist[u] + w < dist[v]
    dist[v] = dist[u] + w
```

---

## 🔹 2.3 ALGORITHM STEPS (EXAM FORM)

1. Initialize:

   ```
   dist[source] = 0
   all others = ∞
   ```

2. Repeat **(V − 1) times**:

   * For each edge → Relax it

3. Negative Cycle Check:

   * If any edge still relaxes → **negative cycle exists**

---

## ✅ Time Complexity

```
O(V × E)
```

✅ Space Complexity

```
O(V)
```

---

## ✅ Applications of Bellman–Ford

* GPS navigation with penalties
* Network routing (RIP protocol)
* Currency exchange arbitrage detection
* Graphs with negative weights

---

# 🔥 3. UNION–FIND (DISJOINT SET DATA STRUCTURE)

This is the **backbone of Kruskal’s Algorithm** ✅

---

## ✅ Definition

Union–Find is a data structure that keeps track of:

* **Disjoint sets**
* Supports:

  * `Find(x)`
  * `Union(x, y)`

---

## 🔹 3.1 OPERATIONS

---

### ✅ FIND(x)

Returns the **representative (root)** of the set.

---

### ✅ UNION(x, y)

Joins the sets containing `x` and `y`.

---

## 🔹 3.2 TWO OPTIMIZATIONS (VERY IMPORTANT 🔥)

---

### ✅ 1️⃣ Path Compression

While finding root, make all nodes point directly to root.

✅ Makes tree flat → faster operations

---

### ✅ 2️⃣ Union by Rank

Always attach **smaller tree under bigger tree**

✅ Prevents skewed trees

---

## ✅ Time Complexity (With Both Optimizations)

```
O(α(n)) ≈ O(1)
```

(α is inverse Ackermann — nearly constant)

---

## ✅ Applications of Union–Find

* Kruskal’s Algorithm
* Network connectivity
* Cycle detection
* Image processing
* Social network groups

---

# 🔥 4. KRUSKAL’S ALGORITHM (MOST IMPORTANT ALGORITHM 🔥🔥🔥)

---

## ✅ Purpose

Find the **Minimum Spanning Tree (MST)** of a connected, undirected, weighted graph.

---

## ✅ Definition: Minimum Spanning Tree

An MST:

* Connects **all vertices**
* Has **V − 1 edges**
* Has **minimum total weight**
* Contains **no cycles**

---

## 🔹 4.1 PRINCIPLE OF KRUSKAL

1. Sort all edges by **increasing weight**
2. Pick the smallest edge
3. If it **does NOT form a cycle**, include it
4. Repeat until **V − 1 edges chosen**

---

## 🔹 4.2 ROLE OF UNION–FIND IN KRUSKAL

| Task              | Union–Find Use |
| ----------------- | -------------- |
| Cycle detection   | ✅              |
| Component merging | ✅              |
| Fast operations   | ✅              |

---

## 🔹 4.3 ALGORITHM STEPS (EXAM FORM)

1. Sort edges by weight
2. Initialize Union–Find
3. For each edge `(u, v)`:

   * If `Find(u) ≠ Find(v)`

     * Add edge to MST
     * `Union(u, v)`
4. Stop when MST has `V - 1` edges

---

## ✅ Time Complexity

```
O(E log E)
```

(Because sorting dominates)

---

## ✅ Space Complexity

```
O(V)
```

---

## ✅ Applications of Kruskal

* Road & bridge networks
* Circuit design
* Computer networks
* Water pipelines
* Cluster analysis

---

# 🔥 5. COMPARISON QUESTIONS (VERY COMMON)

---

## ✅ Bellman–Ford vs Dijkstra

| Feature          | Bellman–Ford | Dijkstra |
| ---------------- | ------------ | -------- |
| Negative weights | ✅ Yes        | ❌ No     |
| Cycle detection  | ✅ Yes        | ❌ No     |
| Speed            | Slower       | Faster   |

---

## ✅ Kruskal vs Prim (MST)

| Feature         | Kruskal       | Prim           |
| --------------- | ------------- | -------------- |
| Works best for  | Sparse graphs | Dense graphs   |
| Uses            | Edge sorting  | Priority queue |
| Cycle detection | Union–Find    | Not required   |

---

## ✅ Graph Algorithm Summary Table

| Algorithm    | Purpose               | Time       |
| ------------ | --------------------- | ---------- |
| Bellman–Ford | Shortest path         | O(VE)      |
| Union–Find   | Set management        | ~O(1)      |
| Kruskal      | Minimum Spanning Tree | O(E log E) |

---

# 🔹 6. MOST IMPORTANT EXAM QUESTIONS ✅✅✅

---

## ✅ 2 Marks

* Define Graph
* What is MST?
* What is Union–Find?
* What is a negative weight cycle?

---

## ✅ 5 Marks

* Explain Bellman–Ford Algorithm
* Explain Union–Find with example
* Applications of Kruskal
* Difference between Kruskal and Prim

---

## ✅ 10 Marks (🔥 VERY HIGH PROBABILITY)

1. Explain **Bellman–Ford Algorithm with example**
2. Explain **Union–Find with optimizations**
3. Explain **Kruskal’s Algorithm with step-by-step working**
4. Compare **Bellman–Ford & Dijkstra**
5. Minimal Spanning Tree using Kruskal

---

# 📘 **UNIT 6 — RANDOMIZATION (6 HOURS)**

### ✅ Topics Covered:

* Concept of Randomized Algorithms
* **Randomized Quicksort**
* **Randomized Select**
* **Skip Lists**

These algorithms use **randomness to improve average performance and avoid worst-case inputs**.

---

# 🔹 1. RANDOMIZED ALGORITHMS — CORE IDEA

---

## ✅ Definition

A **Randomized Algorithm** is an algorithm that makes **random choices during execution** to improve:

* Average performance
* Simplicity
* Resistance to worst-case inputs

---

### ✅ Two Types of Randomized Algorithms

| Type        | Description                                                   |
| ----------- | ------------------------------------------------------------- |
| Las Vegas   | Always correct result, but running time is random             |
| Monte Carlo | Fast result, but may give wrong answer with small probability |

---

### ✅ Examples in Your Syllabus

* **Randomized Quicksort → Las Vegas**
* **Randomized Select → Las Vegas**
* **Skip Lists → Las Vegas**

✅ All algorithms in your unit are **Las Vegas type** (always correct ✅)

---

### ✅ Advantages of Randomization

✔ Avoids worst-case inputs
✔ Better average performance
✔ Simpler implementation
✔ Used in cryptography, networking, AI

---

# 🔥 2. RANDOMIZED QUICKSORT (VERY IMPORTANT)

---

## 🔹 2.1 REVISION: NORMAL QUICKSORT

* Uses **divide and conquer**
* Picks a **pivot**
* Partitions array into:

  * Left < pivot
  * Right > pivot

---

### ❌ Problem:

If pivot is always bad (like first or last element in sorted array):

```
Worst Case Time = O(n²)
```

---

# ✅ SOLUTION → RANDOMIZED QUICKSORT

---

## ✅ Idea

Instead of a fixed pivot:

> Choose a **random element as pivot**

This makes worst-case **extremely unlikely**.

---

## 🔹 2.2 ALGORITHM STEPS

1. Randomly choose an index `r`
2. Swap `A[r]` with `A[high]`
3. Apply normal partition process
4. Recursively sort left & right subarrays

---

## ✅ Time Complexity

| Case         | Time              |
| ------------ | ----------------- |
| Best case    | O(n log n)        |
| Average case | ✅ **O(n log n)**  |
| Worst case   | O(n²) (very rare) |

✅ In practice → behaves like **O(n log n)** always.

---

## ✅ Space Complexity

```
O(log n)  (Recursive stack)
```

---

## ✅ Advantages

✔ Avoids bad input cases
✔ Faster than Merge Sort in practice
✔ In-place sorting
✔ Widely used in real systems

---

## ✅ Applications

* System sorting functions
* Competitive programming
* Database sorting

---

# 🔥 3. RANDOMIZED SELECT (FIND kᵗʰ SMALLEST ELEMENT)

---

## ✅ Problem Definition

Given an unsorted array, find:

> The **kᵗʰ smallest element**

Example:

```
A = [7, 4, 1, 3, 9, 6]
k = 3 → Answer = 3
```

---

## ✅ Idea Behind Randomized Select

* Based on **Randomized Quicksort Partition**
* After partition:

  * If pivot position = k → answer found
  * Else recurse only on one side

✅ Unlike Quicksort → only one side is explored

---

## 🔹 3.1 ALGORITHM STEPS

1. Choose random pivot
2. Partition array
3. Let pivot index = `i`

* If `i == k` → return A[i]
* If `i > k` → recurse on left
* If `i < k` → recurse on right

---

## ✅ Time Complexity

| Case    | Time              |
| ------- | ----------------- |
| Best    | O(n)              |
| Average | ✅ **O(n)**        |
| Worst   | O(n²) (very rare) |

✅ This is **much faster than sorting the full array**

---

## ✅ Applications

* Median finding
* Statistical analysis
* Ranking systems
* Data mining

---

# 🔥 4. SKIP LIST (MOST IMPORTANT THEORY STRUCTURE 🔥🔥🔥)

---

## ✅ Definition

A **Skip List** is a **probabilistic data structure** that allows:

* Searching
* Insertion
* Deletion

in **O(log n) average time**, like balanced trees, but with:
✅ Simpler implementation

---

### ✅ Idea

Instead of one linked list:

* Multiple levels of linked lists are maintained
* Higher levels “skip” many elements

---

## 🔹 4.1 STRUCTURE OF SKIP LIST

Example (Conceptual):

Level 3 →  1 -------- 9
Level 2 →  1 ---- 5 ---- 9
Level 1 →  1 - 3 - 5 - 7 - 9
Level 0 →  1 2 3 4 5 6 7 8 9

Higher levels have **fewer elements**.

---

## 🔹 4.2 SEARCH IN SKIP LIST

1. Start at **top-left**
2. Move right while value is smaller
3. If next is larger → move down
4. Continue until found or reach bottom

---

## 🔹 4.3 INSERTION IN SKIP LIST

1. Insert in **normal linked list (level 0)**
2. Flip a **coin**:

   * If head → go to next level
   * If tail → stop

✅ This randomness decides the height of towers

---

## 🔹 4.4 DELETION IN SKIP LIST

* Remove the node from all levels
* Very similar to deletion in linked lists

---

## ✅ Time Complexity of Skip List

| Operation | Average    | Worst |
| --------- | ---------- | ----- |
| Search    | O(log n) ✅ | O(n)  |
| Insert    | O(log n) ✅ | O(n)  |
| Delete    | O(log n) ✅ | O(n)  |

✅ Worst case is very rare due to randomness.

---

## ✅ Advantages of Skip Lists

✔ Easier than balanced trees
✔ Dynamic structure
✔ No rotations required
✔ Used in databases & Redis

---

## ❌ Disadvantages

❌ Extra memory for pointers
❌ Dependent on randomness

---

# 🔥 5. RANDOMIZED ALGORITHMS vs DETERMINISTIC ALGORITHMS

| Feature              | Randomized           | Deterministic  |
| -------------------- | -------------------- | -------------- |
| Behavior             | Uses randomness      | Fixed behavior |
| Worst-case guarantee | ❌ No                 | ✅ Yes          |
| Average performance  | ✅ Excellent          | ✅ Good         |
| Example              | Randomized Quicksort | Merge Sort     |

---

# 🔹 6. APPLICATIONS OF RANDOMIZATION

* Cryptography
* Load balancing
* Distributed systems
* AI & ML sampling
* Network routing
* Cache replacement

---

# 🔹 7. COMPLETE TIME COMPLEXITY SUMMARY

| Algorithm            | Best       | Average      | Worst |
| -------------------- | ---------- | ------------ | ----- |
| Randomized Quicksort | O(n log n) | ✅ O(n log n) | O(n²) |
| Randomized Select    | O(n)       | ✅ O(n)       | O(n²) |
| Skip List            | O(log n)   | ✅ O(log n)   | O(n)  |

---

# 🔹 8. MOST IMPORTANT EXAM QUESTIONS ✅✅✅

---

## ✅ 2 Marks

* Define Randomized Algorithm
* What is Skip List?
* Define Randomized Quicksort

---

## ✅ 5 Marks

* Explain Randomized Select
* Explain Skip List with advantages
* Difference between Deterministic & Randomized algorithms

---

## ✅ 10 Marks (🔥 VERY HIGH PROBABILITY)

1. Explain **Randomized Quicksort with time complexity**
2. Explain **Randomized Select Algorithm**
3. Explain **Skip List with operations and complexity**
4. Compare **Skip List and Balanced Trees**

---

# 📘 **UNIT 7 — NETWORK FLOWS & FORD–FULKERSON ALGORITHM (5 HOURS)**

### ✅ Topics Covered:

* Flow Network
* Flow, Capacity, Residual Graph
* Augmenting Path
* **Ford–Fulkerson Algorithm**
* Applications
* Time Complexity

This unit is **small but extremely scoring**, especially for **numerical problems** ✅

---

# 🔹 1. FLOW NETWORK — BASIC CONCEPT

---

## ✅ Definition

A **Flow Network** is a **directed graph**:

```
G = (V, E)
```

With:

* A **source node (S)**
* A **sink node (T)**
* Each edge has a **capacity c(u, v)**

---

### ✅ Rules of Flow Network

1. Graph is **directed**
2. Each edge has **capacity ≥ 0**
3. Flow moves from **S → T**
4. No flow can exceed edge capacity

---

### ✅ Example (Conceptual)

```
S → A → T  
S → B → T
```

Each edge has a fixed capacity.

---

# 🔹 2. FLOW IN A NETWORK

---

## ✅ Definition

A **flow f(u, v)** is the amount of data sent from node `u` to `v` such that:

### ✅ Flow Constraints

1. **Capacity Constraint**

```
0 ≤ f(u, v) ≤ c(u, v)
```

2. **Flow Conservation**
   For every node except S and T:

```
Incoming Flow = Outgoing Flow
```

3. **Total Flow**
   Flow out of source = Flow into sink

---

# 🔹 3. RESIDUAL CAPACITY & RESIDUAL GRAPH (VERY IMPORTANT 🔥)

---

## ✅ Residual Capacity

Remaining capacity on an edge:

```
Residual(u, v) = c(u, v) − f(u, v)
```

---

## ✅ Residual Graph

A graph that shows:

* Remaining forward capacity
* Possible backward flow

✅ This graph is **used to find new augmenting paths**

---

# 🔹 4. AUGMENTING PATH

---

## ✅ Definition

An **Augmenting Path** is a path from **S to T** in the **residual graph** where:

* All edges have **positive residual capacity**

---

### ✅ Why It’s Important?

Each augmenting path allows us to **increase the total flow** ✅

---

# 🔥 5. FORD–FULKERSON ALGORITHM (MOST IMPORTANT 🔥🔥🔥)

---

## ✅ Purpose

To find the **maximum possible flow from source (S) to sink (T)**.

---

## ✅ Core Idea

> Repeatedly find **augmenting paths** and increase the flow until no more exist.

---

## 🔹 5.1 FORD–FULKERSON ALGORITHM STEPS (EXAM FORMAT ✅)

---

### ✅ Step 1:

Initialize all flows to **0**

---

### ✅ Step 2:

Construct the **residual graph**

---

### ✅ Step 3:

Find an **augmenting path** from **S to T**

---

### ✅ Step 4:

Find the **minimum residual capacity (bottleneck)** on that path

---

### ✅ Step 5:

Add this flow to all edges of that path

---

### ✅ Step 6:

Update the residual graph

---

### ✅ Step 7:

Repeat until **no more augmenting paths exist**

---

✅ The final total flow is the **Maximum Flow** ✅

---

# 🔹 5.2 BOTTLENECK CAPACITY

---

## ✅ Definition

The **bottleneck** is the **minimum residual capacity on the augmenting path**.

This value determines:

> How much extra flow can be pushed through that path.

---

# 🔹 5.3 TERMINATION CONDITION

Algorithm stops when:

> ❌ No path exists from **S to T** in residual graph.

At this point → **Maximum Flow is achieved** ✅

---

# 🔹 6. TIME COMPLEXITY OF FORD–FULKERSON

---

| Version                 | Time Complexity    |
| ----------------------- | ------------------ |
| Basic Ford–Fulkerson    | **O(E × MaxFlow)** |
| With BFS (Edmonds–Karp) | **O(V × E²)**      |

✅ Many universities write:

```
O(E × f)
where f = maximum flow
```

---

# 🔥 7. APPLICATIONS OF MAX FLOW (VERY IMPORTANT FOR EXAMS ✅)

---

| Field              | Use                       |
| ------------------ | ------------------------- |
| Computer Networks  | Data packet routing       |
| Transportation     | Traffic flow              |
| Job Assignment     | Bipartite matching        |
| Project Management | Resource allocation       |
| Image Segmentation | Vision processing         |
| Supply Chains      | Distribution optimization |

---

# 🔹 8. MAX FLOW vs MIN CUT THEOREM (THEORY QUESTION ✅)

---

## ✅ Statement

> The **maximum flow** from source to sink is equal to the **minimum cut capacity** of the network.

✅ This theorem guarantees that Ford–Fulkerson always gives the correct answer.

---

# 🔹 9. FORD–FULKERSON vs DIJKSTRA / BELLMAN (COMMON CONFUSION)

| Algorithm      | Purpose                      |
| -------------- | ---------------------------- |
| Dijkstra       | Shortest path                |
| Bellman–Ford   | Shortest path with negatives |
| Ford–Fulkerson | **Maximum Flow**             |

✅ They solve **completely different problems**

---

# 🔹 10. ADVANTAGES & DISADVANTAGES

---

## ✅ Advantages

✔ Simple to understand
✔ Works well for medium graphs
✔ Foundation of many flow algorithms

---

## ❌ Disadvantages

❌ Can be slow for large capacities
❌ Depends on augmenting path selection
❌ Worst case can be inefficient

---

# 🔹 11. COMPLETE SUMMARY TABLE

| Term              | Meaning                  |
| ----------------- | ------------------------ |
| Capacity          | Maximum allowed flow     |
| Flow              | Actual flow through edge |
| Residual Capacity | Remaining capacity       |
| Augmenting Path   | Path to increase flow    |
| Max Flow          | Maximum possible flow    |

---

# 🔹 12. MOST IMPORTANT EXAM QUESTIONS ✅✅✅

---

## ✅ 2 Marks

* Define Flow Network
* What is an Augmenting Path?
* What is Maximum Flow?

---

## ✅ 5 Marks

* Explain Residual Graph
* Explain Bottleneck Capacity
* Applications of Max Flow

---

## ✅ 10 Marks (🔥 GUARANTEED NUMERICAL / THEORY)

1. Explain **Ford–Fulkerson Algorithm with example**
2. Find **Maximum Flow for a given network**
3. Explain **Max–Flow Min–Cut Theorem**
4. Applications of **Network Flow**

---






