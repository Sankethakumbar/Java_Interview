# 📖 Java Interview Handbook

# Topic 13 : Encapsulation

---

# 📌 Definition

**Encapsulation** is the process of wrapping **data (variables)** and **methods** into a single unit (class) while protecting the data using **private** access.

---

# ✨ Syntax

```java
class Student{

    private String name;

    public void setName(String name){
        this.name = name;
    }

    public String getName(){
        return name;
    }

}
```

---

# 📊 Getter vs Setter

| Getter | Setter |
|----------|---------|
| Read Data | Update Data |
| Returns Value | Takes Parameter |
| `getName()` | `setName()` |

---

# 🧠 Mind Map

```text
             ENCAPSULATION
                    │
        ┌───────────┴───────────┐
        │                       │
   Private Data          Public Methods
        │                       │
   Data Hiding          Getter & Setter
        │                       │
        └────────── Controlled Access ──────────┘
```

---

# 💡 Memory Trick

```
Capsule 💊

↓

Data + Methods

↓

Private

↓

Protected
```

---

# ✅ Advantages

- Data Hiding
- Security
- Controlled Access
- Better Maintenance

---

# 🚨 Interview Traps

### Trap 1

```java
private int age;

Student s = new Student();

s.age = 20;
```

❌ Compilation Error

---

### Trap 2

Can another class access a private variable directly?

❌ No

---

### Trap 3

Can a class access its own private variables?

✅ Yes

---

### Trap 4

Can a setter validate data?

✅ Yes

---

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is Encapsulation? | Wrapping data & methods | Single unit |
| Why private? | Data Hiding | Protects data |
| Why Getter? | Read Data | Controlled access |
| Why Setter? | Update Data | Validation |
| Why not public variables? | Prevent invalid data | Better security |
| Can private variables be accessed directly? | ❌ No | Outside class cannot access |
| Can class access its own private members? | ✅ Yes | Same class |

---

# ⚡ 30-Second Revision

```
Encapsulation

↓

Data + Methods

↓

Private

↓

Getter

↓

Setter

↓

Data Hiding

↓

Controlled Access
```

---

# ⚡ 5-Second Revision

```
Encapsulation

↓

Private

↓

Getter

↓

Setter

↓

Security
```