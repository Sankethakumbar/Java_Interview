# 📖 Java Interview Handbook

# Topic 14 : Abstraction

---

# 📌 Definition

**Abstraction** is the process of **hiding implementation details** and **showing only the essential functionality**.

### Simple Meaning

```
Know WHAT

❌ Not HOW
```

---

# 🌍 Real-Life Examples

### 🚗 Car

```
Accelerator → Car Moves

Brake → Car Stops

❌ Engine Working Hidden
```

### 🏧 ATM

```
Withdraw Money

Check Balance

❌ Banking Logic Hidden
```

---

# 🧠 Main Idea

```
Parent Class

↓

Declares WHAT to do

↓

Child Class

↓

Implements HOW to do
```

---

# 📌 How is Abstraction Achieved?

```
Abstraction

        │
        ▼
 ┌───────────────┐
 │ Abstract Class│
 └───────────────┘
        │
        ▼
 ┌───────────────┐
 │   Interface   │
 └───────────────┘
```

---

# 📌 Abstract Class

An **abstract class** is a class declared using the `abstract` keyword.

```java
abstract class Animal{

}
```

❌ Cannot create an object.

---

# 📌 Abstract Method

A method without implementation.

```java
abstract void sound();
```

- No body `{ }`
- Ends with `;`

---

# ✨ Example

```java
abstract class Animal{

    abstract void sound();

    void eat(){
        System.out.println("Eating");
    }

}

class Dog extends Animal{

    @Override
    void sound(){
        System.out.println("Bark");
    }

}
```

Output

```java
Dog d = new Dog();

d.eat();
d.sound();
```

```
Eating
Bark
```

---

# 📊 Abstract Class Features

| Feature | Allowed? |
|----------|----------|
| Object Creation | ❌ No |
| Constructor | ✅ Yes |
| Instance Variables | ✅ Yes |
| Normal Methods | ✅ Yes |
| Abstract Methods | ✅ Yes |

---

# 📊 Normal Class vs Abstract Class

| Normal Class | Abstract Class |
|--------------|----------------|
| Can create object | Cannot create object |
| All methods implemented | Can have abstract methods |
| Knows WHAT & HOW | Knows WHAT only |

---

# 🧠 Mind Map

```text
                 ABSTRACTION
                       │
        Hide Implementation Details
                       │
              Show Essential Features
                       │
        ┌──────────────┴──────────────┐
        │                             │
  Abstract Class                 Interface
        │
        ▼
 Cannot Create Object
        │
        ▼
 Can Have
 ├── Constructor
 ├── Variables
 ├── Normal Methods
 └── Abstract Methods
        │
        ▼
 Child Class Must
 Implement Abstract Methods
```

---

# 💡 Memory Tricks

### Trick 1

```
WHAT

↓

Abstract Class

↓

HOW

↓

Child Class
```

---

### Trick 2

```
Abstract Class

↓

Incomplete Class

↓

Child Completes It
```

---

# 🚨 Interview Traps

### Trap 1

Can we create an object?

❌ No

---

### Trap 2

Can an abstract class have a constructor?

✅ Yes

Reason:

Used when child object is created.

---

### Trap 3

Can an abstract class have variables?

✅ Yes

---

### Trap 4

Can it have normal methods?

✅ Yes

---

### Trap 5

Can it have abstract methods?

✅ Yes

---

### Trap 6

If a child class doesn't implement all abstract methods?

➡️ Child class must also be `abstract`.

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is Abstraction? | Hiding implementation | Shows only essential functionality |
| How is it achieved? | Abstract Class & Interface | Java mechanisms |
| Can we create an object of an abstract class? | ❌ No | Incomplete implementation |
| Can it have constructors? | ✅ Yes | Parent initialization |
| Can it have variables? | ✅ Yes | Shared data |
| Can it have normal methods? | ✅ Yes | Common implementation |
| Can it have abstract methods? | ✅ Yes | Force child implementation |
| Why use abstraction? | Reduce complexity | Hide unnecessary details |

---

# ⚡ 30-Second Revision

```
Abstraction

↓

Hide HOW

↓

Show WHAT

↓

Abstract Class

↓

No Object

↓

Constructor ✔

Variables ✔

Normal Methods ✔

Abstract Methods ✔

↓

Child Implements
```

---

# ⚡ 5-Second Revision

```
Abstraction

↓

WHAT

↓

Not HOW

↓

No Object

↓

Child Implements
```