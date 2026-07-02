# 📖 Java Interview Handbook

# Topic 6: Upcasting, Downcasting, instanceof & ClassCastException

---

# 📌 One-Line Definitions

| Topic | Definition |
|--------|------------|
| Upcasting | Child object stored in a Parent reference |
| Downcasting | Parent reference converted back to Child reference |
| instanceof | Checks the actual object type |
| ClassCastException | Runtime exception caused by invalid downcasting |

---

# ✨ Syntax

## Upcasting (Automatic)

```java
Animal a = new Dog();
```

✅ Parent Reference ← Child Object

---

## Downcasting (Explicit)

```java
Dog d = (Dog) a;
```

✅ Child Reference ← Parent Reference

---

## Safe Downcasting

```java
if(a instanceof Dog){

    Dog d = (Dog) a;

}
```

---

# 📊 Upcasting vs Downcasting ⭐⭐⭐⭐⭐

| Upcasting | Downcasting |
|------------|-------------|
| Child → Parent | Parent → Child |
| Automatic | Explicit Casting Required |
| Safe | Can throw ClassCastException |
| No Cast Required | `(Child)` Required |

---

# 🧠 Mind Map

```text
                  CASTING
                     │
        ┌────────────┴────────────┐
        │                         │
   Upcasting                Downcasting
        │                         │
 Child → Parent            Parent → Child
        │                         │
 Automatic                 Explicit Cast
        │                         │
      Safe             Use instanceof
                                │
                                ▼
                     Avoid ClassCastException
```

---

# 💡 Memory Tricks

```
UP

↓

Child → Parent

↓

Automatic

↓

Safe
```

---

```
DOWN

↓

Parent → Child

↓

Explicit Cast

↓

Check using instanceof
```

---

# 🚨 Interview Traps

### Trap 1

```java
Animal a = new Dog();
```

✅ Upcasting

---

### Trap 2

```java
Dog d = (Dog) a;
```

✅ Downcasting

---

### Trap 3

```java
Animal a = new Animal();

Dog d = (Dog) a;
```

❌ Runtime Exception

```
ClassCastException
```

Reason:

Actual object is `Animal`, not `Dog`.

---

### Trap 4

```java
Animal a = new Dog();

Dog d = (Dog) a;
```

✅ Valid

Reason:

Actual object is `Dog`.

---

### Trap 5

```java
Animal a = new Dog();

System.out.println(a instanceof Dog);
```

Output

```
true
```

---

### Trap 6

```java
Animal a = new Animal();

System.out.println(a instanceof Dog);
```

Output

```
false
```

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is Upcasting? | Parent reference to Child object | Supports runtime polymorphism |
| What is Downcasting? | Parent reference converted to Child | Access child-specific members |
| Is Upcasting automatic? | ✅ Yes | Every child IS-A parent |
| Is Downcasting automatic? | ❌ No | Java needs explicit cast |
| Why use `instanceof`? | Check object type | Avoid ClassCastException |
| Why does ClassCastException occur? | Invalid downcasting | Wrong object type |
| Is Upcasting safe? | ✅ Yes | Child is always a Parent |
| Is Downcasting safe? | ❌ Not always | Check using `instanceof` |

---

# ⚡ 30-Second Revision

```
Upcasting

↓

Child → Parent

↓

Automatic

↓

Safe

-------------------

Downcasting

↓

Parent → Child

↓

Explicit Cast

↓

Use instanceof

↓

Avoid ClassCastException
```

---

# ⚡ 5-Second Revision

```
Up → Parent

Down → Child

instanceof → Check Type

Wrong Cast → ClassCastException
```