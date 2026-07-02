# 📖 Java Interview Handbook

# Topic 3: Type Casting & Type Promotion

---

# 📌 Definition

**Type Casting** is the process of converting one data type into another.

Example

```java
int x = 10;
double y = x;
```

---

# 📌 Types of Type Casting

```
Type Casting
│
├── Widening (Implicit)
│
└── Narrowing (Explicit)
```

---

# 📌 Widening Casting (Implicit)

Converts a **smaller data type** into a **larger data type**.

No casting is required.

### Syntax

```java
smallType variable;

bigType newVariable = variable;
```

### Example

```java
int x = 10;

double y = x;
```

✅ Valid

---

### More Examples

```java
byte b = 10;

int x = b;
```

```java
int a = 100;

long l = a;
```

```java
float f = 10.5f;

double d = f;
```

All are valid.

---

# 📌 Narrowing Casting (Explicit)

Converts a **larger data type** into a **smaller data type**.

Casting is mandatory.

### Syntax

```java
smallType variable = (smallType) value;
```

### Example

```java
double d = 10.5;

int x = (int)d;
```

Output

```
10
```

Decimal part is removed.

---

# 📌 Type Promotion

Whenever Java performs arithmetic operations

```
+
-
*
/
%
```

Java automatically promotes

```
byte
short
char
```

to

```
int
```

before calculation.

Example

```java
byte a = 10;

byte b = 20;

int c = a + b;
```

✅ Valid

---

```java
byte c = a + b;
```

❌ Compilation Error

Because

```
byte + byte

↓

int
```

---

# 📊 Widening vs Narrowing

| Widening | Narrowing |
|-----------|------------|
| Small → Big | Big → Small |
| Automatic | Explicit Casting Required |
| Safe | Possible Data Loss |
| No Cast Needed | Cast Needed |

---

# 🧠 Mind Map

```text
                 TYPE CASTING
                       │
          ┌────────────┴────────────┐
          │                         │
      Widening                 Narrowing
          │                         │
  Small → Big               Big → Small
          │                         │
   Automatic               Explicit Cast
          │
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

---

# 💡 Memory Tricks

## Trick 1

```
Small

↓

Big

Automatic
```

---

## Trick 2

```
Big

↓

Small

Needs Casting
```

---

## Trick 3

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

---

# 🚨 Interview Traps

## Trap 1

```java
double d = 10.5;

int x = d;
```

❌ Compilation Error

Correct

```java
int x = (int)d;
```

---

## Trap 2

```java
float f = 10;

double d = f;
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

## Trap 3

```java
double d = 10.5f;
```

✅ Valid

Reason

```
float

↓

double
```

---

## Trap 4

```java
byte a = 10;

byte b = 20;

byte c = a + b;
```

❌ Compilation Error

Reason

```
byte + byte

↓

int
```

---

## Trap 5

```java
byte a = 10;

int c = a + 1;
```

✅ Valid

---

## Trap 6

```java
byte a = 10;

a = a + 1;
```

❌ Compilation Error

Reason

```
a + 1

↓

int

Cannot assign int to byte.
```

---

## Trap 7 ⭐⭐⭐⭐⭐

```java
byte a = 10;

a += 1;
```

✅ Valid

Java automatically performs the cast.

Internally

```java
a = (byte)(a + 1);
```

---

## Trap 8 ⭐⭐⭐⭐⭐

```java
byte a = 10;

a++;
```

✅ Valid

Internally

```java
a = (byte)(a + 1);
```

---

## Trap 9 ⭐⭐⭐⭐⭐

```java
char a = 'A';

char b = 'B';

System.out.println(a + b);
```

Output

```
131
```

Because

```
'A'

↓

65

'B'

↓

66

65 + 66 = 131
```

---

# ⭐ Frequently Asked Interview Questions

### Q1. What is Type Casting?

Conversion of one data type into another.

---

### Q2. Difference between Widening and Narrowing?

| Widening | Narrowing |
|-----------|------------|
| Small → Big | Big → Small |
| Automatic | Manual |
| No Cast | Cast Required |

---

### Q3. What is Type Promotion?

Java automatically converts

```
byte
short
char
```

into

```
int
```

during arithmetic operations.

---

### Q4. Why does `byte + byte` return int?

Because Java promotes both operands to `int` before performing arithmetic.

---

### Q5. Why does `a = a + 1` fail?

Because

```
a + 1

↓

int
```

and Java does not automatically convert `int` back to `byte`.

---

### Q6. Why does `a += 1` work?

Because Java automatically casts the result back to the original type.

---

### Q7. Why does `a++` work?

`++` is a special operator.

Java automatically casts the result back.

---

# 📝 Interview Questions with Answers

## Easy

- What is Type Casting?
- What is Widening?
- What is Narrowing?

---

## Medium

- Difference between Widening and Narrowing.
- Which conversion is automatic?
- Which conversion may lose data?

---

## Hard

- Why does `byte + byte` become `int`?
- Why does `a = a + 1` fail?
- Why does `a += 1` work?
- Why does `a++` work?
- Why does `char + char` return `int`?

---

# 🎯 Interview Cheat Sheet

```
Widening

Small → Big

Automatic

-------------------

Narrowing

Big → Small

Cast Required

-------------------

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

-------------------

Type Promotion

byte
short
char

↓

int

-------------------

a = a + 1

❌

a += 1

✅

a++

✅

char + char

↓

int
```

---

# ⚡ 5-Second Revision

```
Small → Big ✅

Big → Small ❌ Cast

byte + byte = int

short + short = int

char + char = int

a = a + 1 ❌

a += 1 ✅

a++ ✅

char 65 = A
```

---

# ⭐ Top Interview Traps

- `byte + byte = int`
- `char + char = int`
- `a = a + 1` ❌
- `a += 1` ✅
- `a++` ✅
- `double → int` requires casting
- Widening is automatic
- Narrowing requires explicit casting