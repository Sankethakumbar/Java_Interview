# 📖 Java Interview Handbook

# Topic 12 : Polymorphism

---

# 📌 Definition

**Polymorphism** means **one interface, many forms.**

It allows the **same method** to behave differently depending on the object.

---

# 📊 Types of Polymorphism

| Type | Achieved By | Decision Taken |
|------|-------------|----------------|
| Compile-Time | Method Overloading | Compile Time |
| Runtime | Method Overriding | Runtime |

---

# 🧠 Flow of Runtime Polymorphism ⭐⭐⭐⭐⭐

```text
Inheritance
      │
      ▼
Method Overriding
      │
      ▼
Upcasting
      │
      ▼
Dynamic Method Dispatch
      │
      ▼
Runtime Polymorphism
```

---

# ✨ Syntax

## Compile-Time Polymorphism (Overloading)

```java
class Calculator{

    int add(int a,int b){
        return a+b;
    }

    int add(int a,int b,int c){
        return a+b+c;
    }

}
```

---

## Runtime Polymorphism (Overriding)

```java
class Animal{

    void sound(){
        System.out.println("Animal");
    }

}

class Dog extends Animal{

    @Override
    void sound(){
        System.out.println("Dog");
    }

}

public class Main{

    public static void main(String[] args){

        Animal a = new Dog();

        a.sound();

    }

}
```

Output

```
Dog
```

---

# 📊 Compile-Time vs Runtime ⭐⭐⭐⭐⭐

| Compile-Time | Runtime |
|--------------|---------|
| Method Overloading | Method Overriding |
| Same Class | Parent & Child |
| Different Parameters | Same Signature |
| Compiler Decides | JVM Decides |
| Faster | Dynamic Method Dispatch |

---

# 📊 Reference vs Object ⭐⭐⭐⭐⭐

| Reference Decides | Object Decides |
|-------------------|----------------|
| What can be accessed | What actually executes |

Example

```java
Animal a = new Dog();

a.sound();   // Dog

// a.bark(); ❌
```

---

# 🧠 Mind Map

```text
                 POLYMORPHISM
                       │
          ┌────────────┴────────────┐
          │                         │
     Compile-Time              Runtime
          │                         │
   Method Overloading     Method Overriding
          │                         │
   Different Parameters      Same Signature
          │                         │
  Compiler Decides          JVM Decides
                                   │
                            Dynamic Method Dispatch
```

---

# 💡 Memory Tricks

```
Compile-Time

↓

Overloading

↓

Different Parameters
```

---

```
Runtime

↓

Overriding

↓

Same Signature
```

---

```
Reference

↓

Accessible Methods

--------------------

Object

↓

Executed Method
```

---

# 🚨 Interview Traps

### Trap 1

```java
Animal a = new Dog();

a.sound();
```

✅ Dog

Reason:

Object decides execution.

---

### Trap 2

```java
Animal a = new Dog();

a.bark();
```

❌ Compilation Error

Reason:

Reference is Animal.

---

### Trap 3

Can constructors be overridden?

❌ No

---

### Trap 4

Can static methods be overridden?

❌ No

(Method Hiding)

---

### Trap 5

Can final methods be overridden?

❌ No

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is Polymorphism? | One interface, many forms | Same method behaves differently |
| Types of Polymorphism? | Compile-Time & Runtime | Based on decision time |
| Compile-Time achieved by? | Method Overloading | Compiler decides |
| Runtime achieved by? | Method Overriding | JVM decides |
| Why is Runtime Polymorphism called Dynamic Method Dispatch? | Method selected at runtime | Depends on actual object |
| What decides accessible methods? | Reference | Compile-time checking |
| What decides executed method? | Object | Runtime decision |
| Can constructors be overridden? | ❌ No | Constructors aren't inherited |
| Can static methods be overridden? | ❌ No | Method Hiding |
| Can final methods be overridden? | ❌ No | Restricted by `final` |

---

# ⚡ 30-Second Revision

```
Polymorphism

↓

Compile-Time
↓

Overloading
↓

Different Parameters

----------------------

Runtime
↓

Overriding
↓

Same Signature

↓

Inheritance

↓

Upcasting

↓

Dynamic Method Dispatch

----------------------

Reference

↓

Accessible Methods

----------------------

Object

↓

Executed Method
```

---

# ⚡ 5-Second Revision

```
Overloading

↓

Compile Time

↓

Different Parameters

-------------------

Overriding

↓

Runtime

↓

Same Signature

-------------------

Reference → Access

Object → Execute
```