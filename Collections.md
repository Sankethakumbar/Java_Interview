# 📖 Java Interview Handbook

# Topic 17 : Collections Framework

---

# 📌 Definition

The **Collections Framework** is a set of **classes and interfaces** used to **store and manipulate groups of objects dynamically.**

### Simple Definition

> Collections are **dynamic data structures** used to store multiple objects.

---

# 🤔 Why Collections?

## Arrays

```
✔ Fixed Size

✔ Fast

❌ Cannot Grow
```

## Collections

```
✔ Dynamic Size

✔ Easy Insert/Delete

✔ Ready-made Data Structures
```

---

# 🧠 Collection Hierarchy

```
                    Collection
                         │
       ┌─────────────────┼─────────────────┐
       │                 │                 │
      List              Set             Queue
```

> **Note:** `Map` is **NOT** a child of Collection.

---

# 📌 List

### Features

```
✔ Ordered

✔ Duplicates Allowed

✔ Index Based
```

Examples

- ArrayList
- LinkedList
- Vector

---

# 📌 Set

### Features

```
✔ Unique Elements

❌ No Duplicates

❌ No Index
```

Examples

- HashSet
- LinkedHashSet
- TreeSet

---

# 📌 Queue

### Features

```
FIFO

↓

First In

First Out
```

Example

- PriorityQueue

---

# 📌 Map

Stores data as

```
Key → Value
```

### Features

```
Keys

↓

Unique

----------------

Values

↓

Can Duplicate
```

Examples

- HashMap
- LinkedHashMap
- TreeMap

---

# 📊 ArrayList vs LinkedList

| ArrayList | LinkedList |
|------------|------------|
| Dynamic Array | Doubly Linked List |
| Fast Random Access | Slow Random Access |
| Slow Insert/Delete | Fast Insert/Delete |
| Less Memory | More Memory |

### Memory Trick

```
ArrayList

↓

Searching

↓

Fast

--------------------

LinkedList

↓

Insertion

↓

Fast
```

---

# 📊 HashSet vs LinkedHashSet vs TreeSet

| HashSet | LinkedHashSet | TreeSet |
|----------|---------------|----------|
| Random Order | Insertion Order | Sorted Order |
| Fast | Fast | Slightly Slower |

### Memory Trick

```
Hash

↓

Random

------------------

Linked

↓

Insertion Order

------------------

Tree

↓

Sorted
```

---

# 📊 HashMap vs LinkedHashMap vs TreeMap

| HashMap | LinkedHashMap | TreeMap |
|----------|---------------|----------|
| Random Order | Insertion Order | Sorted Keys |
| Fastest | Fast | Slower |

### Memory Trick

```
Hash

↓

Random

------------------

Linked

↓

Insertion Order

------------------

Tree

↓

Sorted
```

---

# 📌 Vector

Vector is similar to ArrayList but

✅ Synchronized

Therefore

❌ Slower

---

# 📊 ArrayList vs Vector

| ArrayList | Vector |
|------------|---------|
| Not Synchronized | Synchronized |
| Faster | Slower |
| Preferred | Older Class |

---

# 📌 Collection vs Collections ⭐⭐⭐⭐⭐

Many students confuse these.

## Collection

```
Interface

↓

Parent of

List

Set

Queue
```

---

## Collections

```
Utility Class

↓

Provides Methods

sort()

reverse()

shuffle()

binarySearch()
```

### Easy Trick

```
Collection

↓

Stores Data

--------------------

Collections

↓

Utility Methods
```

---

# 📌 Collection vs Collections Framework

## Collection

One Interface.

## Collections Framework

Entire framework including

```
Interfaces

↓

Classes

↓

Algorithms
```

Example

```
List

Set

Queue

Map

ArrayList

HashSet

HashMap

Collections Class
```

---

# 📌 Collection vs Map

| Collection | Map |
|------------|-----|
| Stores only Values | Stores Key-Value Pair |
| Parent of List, Set, Queue | Separate Interface |
| Duplicate values allowed | Duplicate Keys NOT allowed |

---

# 📌 Comparable vs Comparator

## Comparable

Used for **natural/default sorting**.

Example

```
Roll Number

Age

Name
```

Method

```java
compareTo()
```

---

## Comparator

Used for **custom sorting**.

Example

```
Sort by Salary

Sort by Marks

Sort by Name Length
```

Method

```java
compare()
```

---

# 📊 Comparable vs Comparator

| Comparable | Comparator |
|-------------|------------|
| Default Sorting | Custom Sorting |
| compareTo() | compare() |
| Inside Class | Separate Class/Object |

---

# 🧠 Mind Map

```
                 COLLECTIONS

                        │

        Dynamic Data Structures

                        │

      ┌──────────┬──────────┬──────────┐
      │          │          │
     List       Set      Queue
      │          │          │
Duplicates   Unique     FIFO

                        │

                      Map

                  Key → Value
```

---

# 🧠 Easy Memory Map

```
List

↓

Ordered

Duplicates

---------------------

Set

↓

Unique

---------------------

Queue

↓

FIFO

---------------------

Map

↓

Key → Value
```

---

# 🧠 Hash Memory Trick

```
Hash

↓

Random

---------------------

Linked

↓

Insertion Order

---------------------

Tree

↓

Sorted
```

Works for both

✔ Set

✔ Map

---

# ⭐ Interview Questions

| Question | Answer |
|----------|--------|
| Parent Interface? | Collection |
| Is Map child of Collection? | ❌ No |
| Which allows duplicates? | List |
| Which stores unique elements? | Set |
| Queue follows? | FIFO |
| Fast random access? | ArrayList |
| Fast insertion/deletion? | LinkedList |
| Random order? | HashSet / HashMap |
| Insertion order? | LinkedHashSet / LinkedHashMap |
| Sorted order? | TreeSet / TreeMap |
| Duplicate Keys? | ❌ No |
| Duplicate Values? | ✅ Yes |
| Synchronized List? | Vector |
| Collection vs Collections? | Interface vs Utility Class |
| Comparable? | Default Sorting |
| Comparator? | Custom Sorting |

---

# 🎯 Which Collection Should I Use?

| Situation | Use |
|-----------|-----|
| Need duplicates + indexing | ArrayList |
| Frequent insert/delete | LinkedList |
| Need unique elements | HashSet |
| Need unique + sorted | TreeSet |
| Need key-value pair | HashMap |
| Need insertion order | LinkedHashMap |
| Need sorted keys | TreeMap |
| Need synchronization | Vector |

---

# ⚡ 30-Second Revision

```
Collection

↓

List

↓

Duplicates

--------------------

Set

↓

Unique

--------------------

Queue

↓

FIFO

--------------------

Map

↓

Key → Value

--------------------

Hash

↓

Random

Linked

↓

Insertion

Tree

↓

Sorted
```

---

# ⚡ 5-Second Revision

```
List → Duplicates

Set → Unique

Queue → FIFO

Map → Key-Value

Hash → Random

Linked → Insertion

Tree → Sorted
```