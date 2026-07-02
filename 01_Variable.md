# 📖 Java Interview Handbook

# Topic 1: Variables

---

# 📌 Definition

A **variable** is a named memory location used to store data.

### Syntax

```java
datatype variableName = value;
```

### Example

```java
int age = 22;
double salary = 45000.50;
char grade = 'A';
boolean isPlaced = true;
```

---

# 📌 Types of Variables

| Feature | Local Variable | Instance Variable | Static Variable |
|----------|---------------|-------------------|-----------------|
| Declaration | Inside method | Inside class | Inside class using `static` |
| Memory | Stack | Heap | Method Area (Class Level) |
| Default Value | ❌ No | ✅ Yes | ✅ Yes |
| Lifetime | Till method ends | Till object exists | Till program ends |
| Copies | Every method call | One per object | One per class |
| Object Required | ❌ No | ✅ Yes | ❌ No |

---

# 🧠 Mind Map

```text
                    VARIABLES
                         │
        ┌────────────────┼────────────────┐
        │                │                │
      Local          Instance         Static
        │                │                │
 Inside Method     Inside Class     static keyword
        │                │                │
 Stack Memory      Heap Memory      Method Area
        │                │                │
 No Default      Default Value      One Copy
        │                │                │
 Short Lifetime  Object Specific    Shared by All Objects
```

---

# 💡 Memory Tricks

## Trick 1

```
L → Local → Lives Little

I → Instance → Individual Object

S → Static → Shared
```

---

## Trick 2 (Classroom Analogy)

```
Teacher  = Static
Student  = Instance
Notebook = Local
```

- One teacher teaches everyone → Static
- Every student is different → Instance
- Notebook exists only during class → Local

---

# 📌 Default Values

| Data Type | Default Value |
|------------|--------------|
| byte | 0 |
| short | 0 |
| int | 0 |
| long | 0L |
| float | 0.0f |
| double | 0.0 |
| char | '\u0000' |
| boolean | false |
| Object/String | null |

> **Note**
>
> Only **Instance** and **Static** variables get default values.
>
> Local variables **must be initialized** before use.

---

# 🚨 Interview Traps

## Trap 1

```java
void show() {
    int x;
    System.out.println(x);
}
```

### Answer

❌ Output = 0

✅ Compilation Error

**Reason**

Local variables do **not** get default values.

---

## Trap 2

```java
class Test {
    int x;
}
```

### Value of x

```
0
```

Reason:

Instance variables get default values.

---

## Trap 3

```java
static int x;
```

### Number of copies?

```
One
```

Reason:

Static variables are shared by every object.

---

## Trap 4

```java
class Test {

    int x = 5;

    public static void main(String[] args) {

        System.out.println(x);

    }
}
```

### Answer

❌ 5

❌ 0

✅ Compilation Error

Reason

```
main() is static

x is instance

Need object
```

Correct

```java
Test t = new Test();

System.out.println(t.x);
```

---

## Trap 5

```java
class Test {

    static int x = 5;

    void show() {

        int x = 10;

        System.out.println(x);

    }
}
```

### Output

```
10
```

Reason

```
Local > Instance > Static
```

Nearest variable wins.

This is called **Variable Shadowing**.

---

# ⭐ Frequently Asked Interview Questions

### Q1. Difference between Local and Instance Variable?

| Local | Instance |
|--------|-----------|
| Inside method | Inside class |
| Stack | Heap |
| No default value | Default value |
| Method scope | Object scope |

---

### Q2. Why don't Local Variables have default values?

Because Java forces the programmer to initialize them to avoid unpredictable behavior.

---

### Q3. Can a static method access an instance variable?

❌ No

Need an object.

```java
Test t = new Test();

System.out.println(t.x);
```

---

### Q4. Why is Static called a Class Variable?

Because it belongs to the **class**, not to individual objects.

---

### Q5. Can we access a static variable using an object?

✅ Yes

```java
student.college;
```

But recommended

```java
Student.college;
```

---

# 🎯 Interview Cheat Sheet

```
Variables

✔ Local
• Stack
• No Default Value
• Method Scope

✔ Instance
• Heap
• Default Value
• Object Specific

✔ Static
• One Copy
• Shared
• Class Level

Priority

Local
↓
Instance
↓
Static

Nearest Variable Wins

Static Method

❌ Cannot access Instance Variable

Need Object
```

---

# ⚡ 5-Second Revision

```
Variables

L → Local → Stack → No Default

I → Instance → Heap → Default

S → Static → Shared → One Copy

Priority

Local > Instance > Static

Static Method ❌ Instance Variable

Need Object
```

---

# 🎯 Interview MCQs

### Easy

- What is the default value of an instance variable?
- Which variable is stored in Stack memory?
- Which variable belongs to an object?
- How many copies of a static variable exist?

### Medium

- Can a static method access an instance variable?
- Can we access a static variable using an object?

### Hard

- Variable Shadowing
- Static Context
- Default Values
- Compilation Errors