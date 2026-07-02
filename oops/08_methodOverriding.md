# 📖 Java Interview Handbook

# Topic 11 : Method Overriding

---

# 📌 Definition

**Method Overriding** means a child class provides its own implementation of a parent class method.

✔ Runtime Polymorphism

---

# ✨ Syntax

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
```

---

# 📌 Rules

✅ Same method name

✅ Same parameters

✅ Inheritance required

✅ Runtime Polymorphism

❌ Cannot override constructors

❌ Cannot override static methods

❌ Cannot override final methods

---

# 📊 Overloading vs Overriding ⭐⭐⭐⭐⭐

| Overloading | Overriding |
|-------------|------------|
| Same Class | Parent & Child |
| Different Parameters | Same Parameters |
| Compile Time | Runtime |
| Inheritance Not Required | Inheritance Required |

---

# 🧠 Mind Map

```text
            METHOD OVERRIDING
                    │
              Parent Method
                    │
              Child Redefines
                    │
             Same Signature
                    │
          Runtime Polymorphism
```

---

# 💡 Memory Trick

```
Overriding

↓

Same Signature

↓

Child Changes Parent Method

↓

Runtime
```

---

# 🚨 Interview Traps

### Trap 1

```java
static void show(){}
```

Can override?

❌ No

Method Hiding.

---

### Trap 2

```java
final void show(){}
```

Override?

❌ No

---

### Trap 3

Constructors

Override?

❌ No

---

### Trap 4

```java
Animal a = new Dog();

a.sound();
```

Output

```
Dog
```

Runtime decides.

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is Method Overriding? | Child redefines parent method | Runtime polymorphism |
| Is inheritance required? | ✅ Yes | Parent method needed |
| Same parameters? | ✅ Yes | Same signature |
| Can constructors be overridden? | ❌ No | Constructors are not inherited |
| Can static methods be overridden? | ❌ No | Method hiding |
| Can final methods be overridden? | ❌ No | Restricted by `final` |
| When is overriding decided? | Runtime | Actual object decides |

---

# ⚡ 30-Second Revision

```
Parent

↓

Child

↓

Same Signature

↓

Runtime

↓

Object Decides
```

---

# ⚡ 5-Second Revision

```
Overriding

↓

Parent + Child

↓

Same Signature

↓

Runtime
```