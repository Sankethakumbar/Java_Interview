# 📖 Java Interview Handbook

# Topic 10 : Method Overloading

---

# 📌 Definition

**Method Overloading** means having **multiple methods with the same name but different parameters** in the same class.

✔ Compile-Time Polymorphism

---

# ✨ Syntax

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

# 📌 Rules

✅ Same method name

✅ Different parameters

- Different number of parameters
- Different data types
- Different order of parameters

❌ Return type alone cannot overload a method.

---

# 📊 Valid vs Invalid

| Valid | Invalid |
|--------|----------|
| Different parameters | Same parameters |
| Different datatype | Only return type changes |
| Different number of parameters | Same signature |

---

# 🧠 Mind Map

```text
            METHOD OVERLOADING
                    │
            Same Method Name
                    │
      ┌─────────────┼─────────────┐
      │             │             │
 Different      Different      Different
 Count          Data Type      Order
                    │
          Compile-Time Polymorphism
```

---

# 💡 Memory Trick

```
Overloading

↓

Same Name

↓

Different Parameters

↓

Compiler Decides
```

---

# 🚨 Interview Traps

### Trap 1

```java
void show(int a){}

void show(int b){}
```

❌ Invalid

Same parameter type.

---

### Trap 2

```java
int show(){

}

double show(){

}
```

❌ Invalid

Return type alone cannot overload.

---

### Trap 3

```java
show(int,double)

show(double,int)
```

✅ Valid

Different order.

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is Method Overloading? | Same method, different parameters | Compile-time polymorphism |
| Can return type overload? | ❌ No | Signature remains same |
| Can parameter order change? | ✅ Yes | Signature changes |
| When is it decided? | Compile Time | Compiler selects method |

---

# ⚡ 30-Second Revision

```
Same Name

↓

Different Parameters

↓

Compile Time

↓

Compiler Chooses
```

---

# ⚡ 5-Second Revision

```
Overloading

↓

Same Name

↓

Different Parameters
```