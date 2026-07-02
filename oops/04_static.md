# 📖 Java Interview Handbook

# Topic 7 : Static

---

# 📌 Definition

**static** means **belongs to the Class, not the Object.**

👉 One copy is shared by all objects.

---

# 🧠 Where can static be used?

| Member | Purpose |
|---------|---------|
| Variable | One copy shared by all objects |
| Method | Called without creating an object |
| Block | Runs once before `main()` |

---

# ✨ Syntax

## Static Variable

```java
class Student{

    static String college = "KLE";

}
```

---

## Static Method

```java
class Student{

    static void show(){
        System.out.println("Hello");
    }

}

Student.show();
```

---

## Static Block

```java
class Test{

    static{
        System.out.println("Static");
    }

    public static void main(String[] args){
        System.out.println("Main");
    }

}
```

Output

```
Static
Main
```

---

# 📊 Static vs Instance ⭐⭐⭐⭐⭐

| Static | Instance |
|---------|----------|
| Class | Object |
| One Copy | One Copy per Object |
| ClassName.member | Object.member |
| No Object Needed | Object Needed |

---

# 🧠 Mind Map

```
                STATIC
                   │
       ┌───────────┼───────────┐
       │           │           │
   Variable      Method      Block
       │           │           │
 One Copy     No Object     Runs Once
   Shared      Needed      Before main()
```

---

# 💡 Easy Memory Trick

```
Static

↓

CLASS

↓

ONE COPY

↓

SHARED
```

Remember

🏫 College = Static

Every student studies in the **same college**

So

```java
static String college="KLE";
```

Perfect example.

---

# 🚨 Interview Traps

### Trap 1

```java
static int x = 10;
```

Copies?

✅ One

---

### Trap 2

```java
int x = 10;

public static void main(String[] args){

    System.out.println(x);

}
```

❌ Compilation Error

Reason

Static method cannot access instance variable directly.

---

### Trap 3

```java
static int x = 10;

public static void main(String[] args){

    System.out.println(x);

}
```

✅ 10

---

### Trap 4

```java
Test t1 = new Test();
Test t2 = new Test();

t1.x = 20;

System.out.println(t2.x);
```

✅ 20

Reason

Only ONE copy exists.

---

### Trap 5

```java
static void show(){

    System.out.println(this);

}
```

❌ Compilation Error

No current object.

---

### Trap 6

```java
static void show(){

    System.out.println(super.toString());

}
```

❌ Compilation Error

No parent object.

---

# ⭐ Most Asked Interview Questions

# ⭐ Most Asked Interview Questions

| Question | Answer | Reason |
|----------|--------|--------|
| What is `static`? | Belongs to Class | Shared by all objects |
| Why use `static`? | Share common data | Saves memory |
| Static variable? | One copy | Shared by every object |
| Static method? | No object required | Belongs to class |
| Can a static method access an instance variable directly? | ❌ No | No current object |
| Can an instance method access a static variable? | ✅ Yes | Instance methods can access class members |
| Can use `this` in a static method? | ❌ No | `this` refers to current object |
| Can use `super` in a static method? | ❌ No | `super` refers to parent object |
| When does a static block execute? | Before `main()` | Runs when class loads |
| How to access a static member? | `ClassName.member` | No object needed |
| How many copies of a static variable exist? | One | Shared across all objects |
| Can we access a static variable using an object? | ✅ Yes (Not Recommended) | Prefer `ClassName.variable` |
---

# ⚡ 30-Second Revision

```
static

↓

Class

↓

One Copy

↓

Shared

-------------------

Variable

↓

One Copy

-------------------

Method

↓

No Object

-------------------

Block

↓

Before main()

-------------------

Static Method

↓

No this

No super

No Instance Variable
```

---

# ⚡ 5-Second Revision

```
Static → Class

One Copy

Shared

No Object

No this

No super
```