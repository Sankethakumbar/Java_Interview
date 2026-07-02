# 📖 Java Interview Handbook

# Topic 6: this, this(), super, super(), final

---

# 📌 One-Line Definitions

| Keyword | Definition |
|----------|------------|
| `this` | Refers to the **current object** |
| `this()` | Calls another constructor of the **same class** |
| `super` | Refers to the **parent class object** |
| `super()` | Calls the **parent class constructor** |
| `final` | Restricts modification |

---

# 📌 Syntax

## this

```java
class Student{

    String name;

    Student(String name){
        this.name = name;
    }

}
```

---

## this()

```java
class Student{

    Student(){
        this(10);
    }

    Student(int x){
        System.out.println(x);
    }

}
```

---

## super

```java
class Animal{

    String color = "White";

}

class Dog extends Animal{

    String color = "Black";

    void show(){
        System.out.println(super.color);
    }

}
```

---

## super()

```java
class Animal{

    Animal(){
        System.out.println("Animal");
    }

}

class Dog extends Animal{

    Dog(){
        super();
        System.out.println("Dog");
    }

}
```

---

## final

```java
final int x = 10;
```

---

# 📊 Comparison Table ⭐⭐⭐⭐⭐

| Keyword | Refers To | Used For | First Statement? |
|----------|-----------|----------|------------------|
| `this` | Current Object | Access current variables/methods | ❌ |
| `this()` | Current Constructor | Constructor Chaining | ✅ |
| `super` | Parent Object | Access parent variables/methods | ❌ |
| `super()` | Parent Constructor | Constructor Chaining | ✅ |
| `final` | Variable / Method / Class | Restrict Modification | ❌ |

---

# 📊 final Types

| final Applied On | Meaning |
|------------------|---------|
| Variable | Cannot change value |
| Method | Cannot override |
| Class | Cannot inherit |

---

# 🧠 Mind Map

```text
                    JAVA KEYWORDS
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
      this              super              final
        │                  │                  │
 Current Object      Parent Object      Restriction
        │                  │                  │
     this()            super()      Variable Method Class
        │                  │
 Same Constructor   Parent Constructor
```

---

# 💡 Memory Tricks

```
this
↓
ME

-------------------

super
↓
MY PARENT

-------------------

()
↓
CONSTRUCTOR

-------------------

final
↓
FREEZE ❄️
```

---

# 🚨 Interview Traps

### Trap 1

```java
this.name = name;
```

✅ Resolves variable shadowing.

---

### Trap 2

```java
this();
```

✅ Must be the **first statement**.

---

### Trap 3

```java
super();
```

✅ Must be the **first statement**.

---

### Trap 4

```java
this();
super();
```

❌ Invalid

Only **one constructor call** is allowed.

---

### Trap 5

```java
static void show(){

    System.out.println(this);

}
```

❌ Compilation Error

---

### Trap 6

```java
static void show(){

    System.out.println(super.x);

}
```

❌ Compilation Error

---

### Trap 7

```java
final Student s = new Student();

s.name = "Rahul";
```

✅ Valid

```java
s = new Student();
```

❌ Invalid

Reason:

Reference is final, object data is mutable.

---

### Trap 8

```java
final class Animal{

}

class Dog extends Animal{

}
```

❌ Compilation Error

---

# ⭐ Frequently Asked Interview Questions

### Q1. Difference between `this` and `this()`?

| `this` | `this()` |
|----------|----------|
| Current Object | Current Constructor |
| Access members | Constructor chaining |

---

### Q2. Difference between `super` and `super()`?

| `super` | `super()` |
|----------|-----------|
| Parent Object | Parent Constructor |
| Access members | Constructor chaining |

---

### Q3. Why can't `this` be used in a static method?

There is **no current object** in a static context.

---

### Q4. Why must `this()` and `super()` be the first statement?

To ensure **constructor chaining** and **proper object initialization**.

---

### Q5. Can `this()` and `super()` be used together?

❌ No

Only one constructor call is allowed.

---

### Q6. Can `this` and `super` be used together?

✅ Yes

Example

```java
System.out.println(this.name);
System.out.println(super.name);
```

---

### Q7. Can a final object be modified?

✅ Yes

Object data can change.

❌ Reference cannot change.

---

# ⚡ 30-Second Revision Card

```
this
↓
Current Object

-------------------

this()
↓
Current Constructor

-------------------

super
↓
Parent Object

-------------------

super()
↓
Parent Constructor

-------------------

final Variable
↓
Cannot Change

final Method
↓
Cannot Override

final Class
↓
Cannot Inherit

final Object
↓
Reference Fixed
Object Mutable
```

---

# ⚡ 5-Second Revision

```
this → ME

this() → MY Constructor

super → PARENT

super() → PARENT Constructor

final → FREEZE
```