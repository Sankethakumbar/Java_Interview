# 📖 Java Interview Handbook

# Topic 4: Class & Object

---

# 📌 Definition

## Class

A **Class** is a blueprint or template used to define the **properties (instance variables)** and **behaviors (methods)** of an object.

A class **does not store actual data**. It only defines what an object should contain.

### Syntax

```java
class Student {

    String name;
    int age;

    void display() {
        System.out.println(name + " " + age);
    }
}
```

---

## Object

An **Object** is a real-world **instance of a class**.

Objects store **actual values**, occupy **heap memory**, and are created using the **new** keyword.

### Syntax

```java
Student s1 = new Student();
```

---

# 📌 Why Do We Need Classes?

Without classes, storing information for thousands of students would require thousands of separate variables.

```java
String name1;
int age1;

String name2;
int age2;

String name3;
int age3;
```

This becomes:

- Difficult to maintain
- Repetitive
- Not reusable
- Poorly organized

Using a class provides a common structure.

```java
class Student {

    String name;
    int age;

}
```

Now we simply create objects.

```java
Student s1 = new Student();
Student s2 = new Student();
Student s3 = new Student();
```

Each object stores different data while following the same structure.

---

# 📌 Relationship

```
Class
        ↓
Blueprint

Object
        ↓
Real Instance
```

One class can create **multiple objects**.

---

# 📌 Memory Representation

Before creating an object

```
Class

Student

name

age
```

No object exists.

No memory for student data is allocated.

---

After

```java
Student s1 = new Student();
```

```
Heap Memory

+----------------+
| name = null    |
| age = 0        |
+----------------+
        ▲
        │
       s1
```

Instance variables receive default values.

---

# 📌 Role of new Keyword

The **new** keyword

- Creates an object
- Allocates memory in Heap
- Returns the object's reference

Example

```java
Student s1 = new Student();
```

---

# 📊 Class vs Object

| Class | Object |
|--------|---------|
| Blueprint | Instance |
| Logical Entity | Physical Entity |
| Defines structure | Stores actual data |
| Created once | Multiple objects can be created |
| No memory for instance data | Occupies Heap Memory |
| Contains variables and methods | Contains actual values |

---

# 🧠 Mind Map

```text
                    OOP
                     │
          ┌──────────┴──────────┐
          │                     │
       Class                 Object
          │                     │
      Blueprint            Real Instance
          │                     │
  Variables + Methods      Stores Data
          │                     │
     No Object Data       Heap Memory
          │                     │
      One Class         Many Objects
```

---

# 💡 Memory Tricks

## Trick 1

```
Class

↓

Blueprint
```

---

## Trick 2

```
Object

↓

House Built Using Blueprint
```

---

## Trick 3

```
One Class

↓

Many Objects
```

---

# 🚨 Interview Traps

## Trap 1

```java
class Student {

    String name;

}
```

How many objects exist?

✅ 0

Only the class is created.

---

## Trap 2

```java
Student s1 = new Student();
```

How many objects exist?

✅ 1

---

## Trap 3

```java
Student s1 = new Student();

Student s2 = new Student();

Student s3 = s2;
```

Objects?

✅ 2

`s3` is another reference to the same object.

---

## Trap 4

```java
Student s1 = null;
```

Object created?

❌ No

Only a reference variable exists.

---

## Trap 5

```java
class Student {

    String name;

}

Student s = new Student();

System.out.println(s.name);
```

Output

```
null
```

Reason

Instance variables receive default values.

---

## Trap 6

```java
class Student {

    int age;

}

Student s = new Student();

System.out.println(s.age);
```

Output

```
0
```

---

# ⭐ Frequently Asked Interview Questions

### Q1. What is a Class?

A class is a blueprint or template that defines the properties and behaviors of an object.

---

### Q2. What is an Object?

An object is the runtime instance of a class that stores actual data and occupies memory.

---

### Q3. Why do we need classes?

Classes help organize code, improve reusability, reduce duplication, and model real-world entities.

---

### Q4. Can one class create multiple objects?

✅ Yes

A single class can create any number of objects.

---

### Q5. Which keyword creates an object?

✅ `new`

---

### Q6. What is the purpose of the `new` keyword?

It allocates memory in the heap and creates an object.

---

### Q7. Where are objects stored?

Objects are stored in **Heap Memory**.

---

### Q8. Does a class occupy heap memory?

❌ No

Objects occupy heap memory.

---

# 📝 Interview Questions with Answers

## Easy

### What is a Class?

A blueprint or template used to create objects.

---

### What is an Object?

An instance of a class.

---

### Which keyword creates an object?

`new`

---

## Medium

### Difference between Class and Object?

A class defines the structure, while an object stores actual values and occupies memory.

---

### Why are classes required?

They provide organization, code reusability, and allow multiple objects with the same structure.

---

## Hard

### Explain the difference between a Class and an Object with an example.

**Answer:**

A class is a blueprint that defines properties and behaviors. It does not store actual object data. An object is the runtime instance of that class, created using the `new` keyword. For example, `Student` is a class, while `Student s1 = new Student();` creates an object representing one specific student.

---

### Why doesn't `Student s = null;` create an object?

Because only a reference variable is created. Memory is allocated only when the `new` keyword is used.

---

# 🎯 Interview Cheat Sheet

```
Class

Blueprint

Properties + Methods

No Actual Data

----------------------

Object

Instance

Stores Actual Values

Heap Memory

----------------------

new

Creates Object

Allocates Memory

Returns Reference

----------------------

One Class

↓

Many Objects
```

---

# ⚡ 30-Second Revision Card

```
Class

Blueprint

No Actual Data

-----------------

Object

Instance

Heap Memory

-----------------

new

Creates Object

Allocates Memory

-----------------

One Class

↓

Many Objects

-----------------

Default Values

String → null

int → 0
```

---

# ⚡ 5-Second Revision

```
Class = Blueprint

Object = Instance

new = Creates Object

Object = Heap

One Class → Many Objects

String → null

int → 0
```

---

# ⭐ Common Mistakes (Based on Today's Session)

❌ Thinking a class itself stores object data.

❌ Confusing a reference variable with an object.

❌ Assuming `Student s = null;` creates an object.

❌ Thinking `Student s3 = s2;` creates a new object.

✅ Remember:

- A class defines the structure.
- `new` creates the object.
- Multiple references can point to the same object.