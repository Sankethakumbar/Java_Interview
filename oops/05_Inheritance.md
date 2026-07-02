# 📖 Java Interview Handbook

# Topic 8 : Inheritance

---

# 📌 Definition

**Inheritance** is the process where one class acquires the properties and methods of another class.

Keyword

```java
extends
```

Purpose

- Code Reusability
- Reduce Code Duplication
- Easy Maintenance
- Represents IS-A Relationship

---

# ✨ Syntax

```java
class Animal{

    void eat(){

    }

}

class Dog extends Animal{

    void bark(){

    }

}
```

---

# 📊 Types of Inheritance

| Type | Java Supports? |
|--------|---------------|
| Single | ✅ |
| Multilevel | ✅ |
| Hierarchical | ✅ |
| Multiple (Classes) | ❌ |
| Hybrid (Classes) | ❌ |

---

# 📊 Parent vs Child

| Parent | Child |
|---------|-------|
| Superclass | Subclass |
| Base Class | Derived Class |
| Gives Properties | Inherits Properties |

---

# 🧠 Mind Map

```text
               INHERITANCE
                    │
             Code Reuse
                    │
        ┌───────────┴───────────┐
        │                       │
   Parent Class            Child Class
   (Superclass)            (Subclass)
        │                       │
        └────── extends ─────────┘
                    │
              IS-A Relationship
```

---

# 💡 Memory Trick

```
Dog

IS-A

Animal

----------------

extends

↓

Inheritance

----------------

Reuse Code
```

---

# 🚨 Interview Traps

### Trap 1

```java
class Dog extends Animal
```

Uses

✅ `extends`

---

### Trap 2

Can Java support

```java
class C extends A,B
```

❌ No

Reason

Diamond Problem

---

### Trap 3

```java
new Dog();
```

Output

```
Animal
Dog
```

Reason

Parent constructor executes first.

---

### Trap 4

Can child access parent's public methods?

✅ Yes

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is inheritance? | Acquiring parent properties | Code Reusability |
| Which keyword? | `extends` | Creates inheritance |
| Why use inheritance? | Reuse code | Reduces duplication |
| Which relationship? | IS-A | Child is a type of parent |
| Does Java support Multiple Inheritance (classes)? | ❌ No | Diamond Problem |
| Can child access parent's public methods? | ✅ Yes | Methods are inherited |
| Which constructor executes first? | Parent | `super()` is called first |

---

# ⚡ 30-Second Revision

```
Inheritance

↓

extends

↓

Code Reuse

↓

IS-A Relationship

↓

Parent

↓

Child

↓

Parent Constructor First

↓

No Multiple Inheritance (Classes)
```

---

# ⚡ 5-Second Revision

```
extends

↓

Reuse Code

↓

IS-A

↓

Parent First

↓

No Multiple Inheritance
```