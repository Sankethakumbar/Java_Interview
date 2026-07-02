# 🧠 Method Signature

## 📌 Definition

A **Method Signature** is the combination of:

- Method Name
- Parameter Types

❌ It does **NOT** include:

- Return Type
- Parameter Names
- Access Modifier
- `static`
- `final`

---

## 📊 Examples

| Method | Signature |
|---------|-----------|
| `void show()` | `show()` |
| `int show()` | `show()` |
| `void show(int a)` | `show(int)` |
| `void show(double a)` | `show(double)` |
| `void show(int a, double b)` | `show(int, double)` |
| `double show(int a, double b)` | `show(int, double)` |

---

## 🧠 Mind Map

```text
              METHOD SIGNATURE
                     │
          ┌──────────┴──────────┐
          │                     │
     Method Name         Parameter Types
          │                     │
          └──────────┬──────────┘
                     │
               Method Signature
                     │
          Ignore Return Type
          Ignore Parameter Names
```

---

## 💡 Memory Trick

```
Signature

↓

Name

+

Parameter Types

❌ Return Type

❌ Variable Names
```

---

## 🚨 Interview Traps

### Trap 1

```java
int show(){}

double show(){}
```

❌ Invalid

Reason:

Same Signature

---

### Trap 2

```java
void show(int a){}

void show(int b){}
```

❌ Invalid

Reason:

Parameter names don't matter.

---

### Trap 3

```java
void show(int a){}

void show(double a){}
```

✅ Valid

Reason:

Parameter types are different.

---

## ⚡ 30-Second Revision

```
Method Signature

↓

Method Name

+

Parameter Types

--------------------

Ignore

❌ Return Type

❌ Parameter Names
```

---

## ⚡ 5-Second Revision

```
Signature

=

Name

+

Parameter Types
```