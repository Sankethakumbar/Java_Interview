# 📖 Java Interview Handbook

# Topic 5: Constructors

---

# 📌 Definition

A **Constructor** is a special member of a class that is automatically called whenever an object is created.

Its primary purpose is to **initialize the object's instance variables**.

---

# 📌 Why Do We Need Constructors?

Without constructors

```java
Student s1 = new Student();

s1.name = "Rahul";
s1.age = 22;
```

Values must be assigned manually.

Problems

- More code
- Repetitive
- Error-prone
- Difficult to maintain

Using constructors

```java
Student s1 = new Student("Rahul",22);
```

Object is initialized during creation.

---

# 📌 Types of Constructors

```
Constructors
│
├── Default Constructor
│      (Provided automatically if no constructor is written)
│
└── User Defined Constructors
       │
       ├── Non-Parameterized Constructor
       │
       └── Parameterized Constructor
```

---

# 📌 Default Constructor

If no constructor is written, Java automatically provides a default constructor.

Example

```java
class Student{

}
```

Internally (conceptually)

```java
class Student{

    Student(){

    }

}
```

---

# 📌 User Defined Non-Parameterized Constructor

```java
class Student{

    Student(){

        System.out.println("Object Created");

    }

}
```

---

# 📌 Parameterized Constructor

```java
class Student{

    String name;
    int age;

    Student(String name,int age){

        this.name = name;
        this.age = age;

    }

}
```

---

# 📌 Rules of Constructor

| Rule | Description |
|------|-------------|
| Same name as class | ✅ Yes |
| No return type | ✅ Yes |
| Automatically called | ✅ Yes |
| Can have parameters | ✅ Yes |
| Can be overloaded | ✅ Yes |
| Cannot be inherited | ✅ Yes |

---

# 📊 Constructor vs Method

| Constructor | Method |
|-------------|--------|
| Initializes object | Performs operation |
| Same name as class | Any valid name |
| No return type | Must have return type / void |
| Called automatically | Called explicitly |
| Can be overloaded | Can be overloaded |
| Cannot be inherited | Can be inherited (subject to access rules) |

---

# 🧠 Mind Map

```text
                    CONSTRUCTOR
                         │
        ┌────────────────┼────────────────┐
        │                │                │
   Default         Non-Parameterized   Parameterized
        │                │                │
 Auto Generated     User Defined     User Defined
        │                │                │
 No Arguments      No Arguments     Arguments
        │                │                │
 Initializes Object Automatically
```

---

# 💡 Memory Tricks

## Trick 1

```
Constructor

↓

Create Object

↓

Initialize Object
```

---

## Trick 2

```
Same Name

↓

Constructor

Different Name

↓

Method
```

---

## Trick 3

```
No Return Type

↓

Constructor

void

↓

Method
```

---

# 🚨 Interview Traps

## Trap 1

```java
class Test{

    void Test(){

    }

}
```

Constructor?

❌ No

It is a method.

---

## Trap 2

```java
class Test{

    Test(){

    }

}
```

Constructor?

✅ Yes

---

## Trap 3

```java
class Student{

    Student(int age){

    }

}

Student s = new Student();
```

Output

❌ Compilation Error

Reason

Default constructor is NOT generated because a user-defined constructor already exists.

---

## Trap 4

```java
class Test{

    Test(){

    }

    Test(int x){

    }

}
```

This is

✅ Constructor Overloading

---

## Trap 5

```java
Test t = new Test();
```

Which executes first?

✅ Constructor

---

# ⭐ Frequently Asked Interview Questions

### Q1. What is a Constructor?

A constructor is a special member of a class used to initialize objects.

---

### Q2. Why do we need Constructors?

Constructors initialize objects automatically, reduce repetitive code, improve readability, and reduce errors.

---

### Q3. Can constructors have a return type?

❌ No

Not even `void`.

---

### Q4. Can constructors be overloaded?

✅ Yes

---

### Q5. Can constructors be inherited?

❌ No

---

### Q6. When is a constructor called?

Automatically when an object is created.

---

### Q7. What happens if we don't write any constructor?

Java provides a default constructor automatically.

---

### Q8. What happens if we write one parameterized constructor?

The default constructor is NOT generated automatically.

---

# 📝 Interview Questions with Answers

## Easy

### What is a Constructor?

A special member of a class that initializes an object.

---

### Why do we use Constructors?

To initialize objects automatically and reduce repetitive code.

---

## Medium

### Difference between Constructor and Method?

Constructors initialize objects and have no return type, whereas methods perform operations and must have a return type or `void`.

---

### Can constructors be overloaded?

Yes, by changing the number or type of parameters.

---

## Hard

### Why doesn't a constructor have a return type?

Because its purpose is object initialization. If a return type is specified (even `void`), it becomes a method.

---

### Why does the following code give a compilation error?

```java
class Student{

    Student(int age){

    }

}

Student s = new Student();
```

Because writing any constructor prevents Java from generating the default constructor automatically.

---

# 🎯 Interview Cheat Sheet

```
Constructor

Same Name as Class

No Return Type

Automatically Called

Initializes Object

------------------------

Default Constructor

Auto Generated

Only if No Constructor Exists

------------------------

User Defined

Non-Parameterized

Parameterized

------------------------

Can Overload

Cannot Inherit
```

---

# ⚡ 30-Second Revision Card

```
Constructor

↓

Initialize Object

---------------------

Same Name

No Return Type

---------------------

Default

Auto Generated

---------------------

Parameterized

Pass Values

---------------------

Method

Return Type

Explicit Call
```

---

# ⚡ 5-Second Revision

```
Constructor = Initialize

Same Name

No Return Type

Auto Call

Can Overload

Cannot Inherit

Default Constructor

↓

Only if No Constructor Exists
```

---

# ⭐ Common Mistakes (Based on Today's Session)

❌ Thinking every no-argument constructor is a default constructor.

✅ A no-argument constructor written by the programmer is a **User Defined Non-Parameterized Constructor**.

❌ Thinking Java always generates a default constructor.

✅ Java generates it **only when no constructor is written**.

❌ Thinking `void Test()` is a constructor.

✅ It is a method because it has a return type.

❌ Forgetting constructors initialize objects.

✅ Constructors are automatically called when an object is created.



                         CONSTRUCTORS
                               │
      ┌────────────────────────┼─────────────────────────┐
      │                        │                         │
  Default               User Defined              Purpose
      │                        │                     │
Auto Generated      ┌──────────┴──────────┐    Initialize Object
(No Constructor)    │                     │
             Non-Parameterized     Parameterized
                    │                     │
              No Arguments         Arguments
                    │                     │
         Same Name as Class • No Return Type
                    │
          Called Automatically by `new`
                    │
         Can Overload • Cannot Inherit