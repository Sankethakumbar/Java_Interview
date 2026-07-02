# 📖 Java Interview Handbook

# Topic 2: Data Types

---

# 📌 Definition

A **Data Type** defines:

- What kind of value a variable can store.
- How much memory is allocated.
- What operations can be performed on the data.

Example

```java
int age = 22;
double salary = 45000.50;
char grade = 'A';
boolean isPlaced = true;
```

---

# 📌 Types of Data Types

Java has **2 categories** of data types.

```
Data Types
│
├── Primitive
│
└── Non-Primitive (Reference)
```

---

# 📌 Primitive Data Types

Java has **8 Primitive Data Types**.

| Data Type | Size | Default Value | Wrapper Class |
|------------|------|---------------|---------------|
| byte | 1 byte | 0 | Byte |
| short | 2 bytes | 0 | Short |
| int | 4 bytes | 0 | Integer |
| long | 8 bytes | 0L | Long |
| float | 4 bytes | 0.0f | Float |
| double | 8 bytes | 0.0 | Double |
| char | 2 bytes | '\u0000' | Character |
| boolean | JVM Dependent | false | Boolean |

---

# 📌 Non-Primitive Data Types

Examples

- String
- Array
- Class
- Object
- Interface
- Enum

Example

```java
String name = "Java";

int[] arr = {1,2,3};

Student s = new Student();
```

---

# 📊 Primitive vs Non-Primitive

| Primitive | Non-Primitive |
|------------|---------------|
| Stores actual value | Stores reference (address) |
| Fixed size | Variable size |
| Faster | Slightly slower |
| Built into Java | Created by programmer/Java |
| Cannot call methods | Methods available |

---

# 🧠 Mind Map

```text
                    DATA TYPES
                         │
          ┌──────────────┴──────────────┐
          │                             │
     Primitive                    Non-Primitive
          │                             │
          │                     String
          │                     Array
          │                     Object
          │                     Class
          │                     Interface
          │
 ┌────────────────────────────────────────────┐
 │ byte short int long float double char boolean │
 └────────────────────────────────────────────┘
```

---

# 💡 Memory Tricks

## Trick 1

Remember the order

```
byte
 ↓
short
 ↓
int
 ↓
long
 ↓
float
 ↓
double
```

Small → Big

Useful for Type Casting.

---


## Trick 2 (Most Important)

```
10

↓

int
```

```
10.5

↓

double
```

```
10.5f

↓

float
```

```
100L

↓

long
```

---

# 🚨 Interview Traps

## Trap 1

```java
float x = 10.5;
```

❌ Compilation Error

Reason

`10.5` is a **double** literal.

Correct

```java
float x = 10.5f;
```

---

## Trap 2

```java
long x = 100;
```

✅ Valid

Reason

```
int → long

Widening
```

---

## Trap 3

```java
long x = 10000000000;
```

❌ Compilation Error

Correct

```java
long x = 10000000000L;
```

---

## Trap 4

```java
char ch = 65;

System.out.println(ch);
```

Output

```
A
```

Because

```
65 = Unicode of A
```

---

## Trap 5

```java
char ch = '65';
```

❌ Compilation Error

Because char stores only one character.

---

## Trap 6

```java
boolean b = 1;
```

❌ Compilation Error

Java doesn't convert integers to boolean.

---

## Trap 7

```java
double d = 10.5f;
```

✅ Valid

Reason

```
float

↓

double

Widening
```

---

# ⭐ Frequently Asked Interview Questions

### Q1. How many primitive data types are there?

**Answer**

8

---

### Q2. Which is the default decimal data type?

**Answer**

double

---

### Q3. Which data types store decimal numbers?

**Answer**

float and double

---

### Q4. Difference between float and double?

| float | double |
|--------|---------|
| 4 bytes | 8 bytes |
| Less Precision | More Precision |
| Needs `f` | No suffix |

---

### Q5. Difference between Primitive and Non-Primitive?

| Primitive | Non-Primitive |
|------------|---------------|
| Stores value | Stores reference |
| Fixed size | Variable size |
| No methods | Methods available |

---

### Q6. Why does float require `f`?

Because decimal literals are **double** by default.

---

### Q7. Why does long require `L`?

Because integer literals are **int** by default.

---

### Q8. Why is `char ch = 65;` valid?

Because char stores Unicode values.

---

# 📝 Interview Questions with Answers

## Easy

### How many primitive data types are there?

**Answer:** 8

---

### Which is the default decimal type?

**Answer:** double

---

### Which data type stores true/false?

**Answer:** boolean

---

### Which data type stores Unicode characters?

**Answer:** char

---

## Medium

### Can we assign an int to a long?

✅ Yes

Widening.

---

### Can we assign a double to a float?

❌ No

Requires explicit casting.

---

### Why is float smaller than double?

Because float uses **4 bytes**, whereas double uses **8 bytes**.

---

## Hard

### Why does this fail?

```java
float f = 10.5;
```

Because `10.5` is double by default.

---

### Why does this work?

```java
char ch = 65;
```

Because Unicode value **65** represents `'A'`.

---

### Why does this work?

```java
double d = 10.5f;
```

Because float → double is widening.

---

# 🎯 Interview Cheat Sheet

```
Primitive = 8

byte
short
int
long
float
double
char
boolean

----------------------

Default Integer → int

Default Decimal → double

----------------------

float → f

long → L

----------------------

char → Unicode

boolean → true/false

----------------------

Primitive → Value

Reference → Address
```

---

# ⚡ 5-Second Revision

```
Primitive = 8

B S I L F D C B

10 → int

10L → long

10.5 → double

10.5f → float

65 → A

Primitive → Value

Reference → Address
```

---

# ⭐ Top Interview Traps

- float requires `f`
- long literals require `L`
- `char 65` prints `A`
- `10.5` is double by default
- `boolean b = 1` ❌
- Primitive stores value
- Reference stores address