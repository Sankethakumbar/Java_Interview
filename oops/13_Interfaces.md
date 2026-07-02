# 📖 Java Interview Handbook

# Topic 15 : Interface

---

# 📌 Definition

An **Interface** is a **contract (set of rules)** that tells a class **what it must do**, but **not how to do it**.

The implementing class provides the implementation.

---

# 🌍 Real-Life Example

### 📱 Mobile Phone

```
Phone CAN

✔ Call

✔ Camera

✔ Play Music

✔ Charge
```

Different companies implement these features differently.

You know **WHAT** it can do, not **HOW** it works internally.

---

# 📌 Why do we need Interface?

- Achieve Abstraction
- Support Multiple Inheritance
- Define Common Rules (Contract)
- Represent Capabilities (CAN-DO Relationship)

---

# 🧠 Main Idea

```
           INTERFACE

                │

         Defines Rules

                │

     No Implementation (Traditionally)

                │

        Class Implements Rules

                │

      Provides Implementation
```

---

# ✨ Syntax

```java
interface Animal{

    void sound();

}

class Dog implements Animal{

    @Override
    public void sound(){

        System.out.println("Bark");

    }

}
```

---

# 📊 Abstract Class vs Interface

| Abstract Class | Interface |
|----------------|-----------|
| Represents WHAT you ARE | Represents WHAT you CAN DO |
| Uses `extends` | Uses `implements` |
| Can have Constructor | No Constructor |
| Can have Instance Variables | No Instance Variables (Only Constants) |
| Can have Normal Methods | Traditionally only Abstract Methods* |
| Single Inheritance | Multiple Interfaces Allowed |

> **Note:** Since Java 8, interfaces can also have `default` and `static` methods. Since Java 9, they can also have `private` methods.

---

# 📊 extends vs implements

| extends | implements |
|----------|------------|
| Inherit Implementation | Follow Contract |
| IS-A Relationship | CAN-DO Relationship |
| One Parent Class | Multiple Interfaces |

---

# 📌 Types of Interfaces

```
                INTERFACE
                     │
         ┌───────────┴───────────┐
         │                       │
  Normal Interface        Marker Interface
```

---

# 1️⃣ Normal Interface

Contains **method declarations**.

Implementing class **must implement** all methods.

```java
interface Animal{

    void sound();

}
```

---

# 2️⃣ Marker Interface (Tag Interface)

Contains **no methods** and **no fields**.

Used only to **mark** a class with a special capability.

```java
interface Serializable{

}
```

Example

```java
class Student implements Serializable{

}
```

Java understands that the object supports serialization.

---

# ⭐ Common Marker Interfaces

| Interface | Purpose |
|------------|---------|
| Serializable | Convert object into byte stream |
| Cloneable | Allow object cloning |
| Remote | Used in Java RMI (Remote Method Invocation) |

---

# 📌 Interface Features

| Feature | Allowed? |
|----------|----------|
| Object Creation | ❌ No |
| Constructor | ❌ No |
| Instance Variables | ❌ No |
| Constants (`public static final`) | ✅ Yes |
| Abstract Methods | ✅ Yes |
| Multiple Inheritance | ✅ Yes |

---

# 🧠 Mind Map

```text
                    INTERFACE
                         │
                 Contract / Rules
                         │
              Defines WHAT to do
                         │
              Class implements HOW
                         │
        ┌────────────────┴────────────────┐
        │                                 │
  Achieves Abstraction          Multiple Inheritance
        │                                 │
        ▼                                 ▼
 Hide Implementation        Multiple Interfaces Allowed
                         (No Diamond Problem)
```

---

# 🧠 Types Mind Map

```text
                 INTERFACE
                      │
        ┌─────────────┴─────────────┐
        │                           │
 Normal Interface           Marker Interface
        │                           │
 Has Methods             No Methods
        │                           │
 Must Implement        Marks a Class
        │                           │
   Example                 Serializable
                            Cloneable
                            Remote
```

---

# 💡 Memory Tricks

### Trick 1

```
Interface

↓

Contract

↓

Rules

↓

Class Implements
```

---

### Trick 2

```
Abstract Class

↓

WHAT ARE YOU?

----------------------

Interface

↓

WHAT CAN YOU DO?
```

---

### Trick 3

```
extends

↓

IS-A

----------------------

implements

↓

CAN-DO
```

---

# 🚨 Interview Traps

### Trap 1

Can we create an object of an Interface?

❌ No

---

### Trap 2

Can Interface have constructors?

❌ No

Reason:

No object is created.

---

### Trap 3

Can Interface have instance variables?

❌ No

Only Constants.

---

### Trap 4

Can one class implement multiple interfaces?

✅ Yes

---

### Trap 5

Why no Diamond Problem?

✅ Interfaces provide contracts, not implementation.

---

### Trap 6

Keyword used?

```
implements
```

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is an Interface? | Contract / Set of Rules | Defines behavior |
| Why use Interface? | Abstraction + Multiple Inheritance | Avoid Diamond Problem |
| Keyword? | `implements` | Implement contract |
| Can create object? | ❌ No | No implementation |
| Can have constructors? | ❌ No | No object creation |
| Can have variables? | ❌ No | Only Constants |
| Multiple Interfaces? | ✅ Yes | No implementation conflict |
| Marker Interface? | Interface with no methods | Marks a class |

---

# ⚡ 30-Second Revision

```
Interface

↓

Contract

↓

Rules

↓

implements

↓

CAN-DO

↓

Multiple Interfaces

↓

No Constructor

↓

No Object

↓

Only Constants

↓

Marker Interface
```

---

# ⚡ 5-Second Revision

```
Interface

↓

Contract

↓

implements

↓

CAN-DO

↓

Multiple Inheritance
```

---

# 🎯 OOP Summary (Remember Forever)

```text
Inheritance
↓

Reuse Code

-------------------------

Encapsulation
↓

Hide Data

-------------------------

Abstraction
↓

Hide Implementation

-------------------------

Interface
↓

Contract + Capabilities

-------------------------

Polymorphism
↓

Same Method
Different Behavior
```