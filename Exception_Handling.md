# 📖 Java Interview Handbook

# Topic 16 : Exception Handling

---

# 📌 Definition

**Exception Handling** is a mechanism in Java used to **handle runtime errors** so that the **normal flow of the program can continue**.

### Simple Definition

> Instead of crashing the program, Java handles the error and continues execution.

---

# 🌍 Real-Life Example

### 🏧 ATM

```
Withdraw Money

↓

Error Occurs

↓

Show Error Message

↓

Continue Using ATM
```

Instead of stopping the whole ATM, only the error is handled.

---

# 🧠 Main Idea

```
Exception Occurs

↓

Catch the Exception

↓

Handle It

↓

Continue Program
```

---

# 📌 Why Exception Handling?

- Prevents program from crashing
- Handles runtime errors
- Improves program reliability
- Allows normal program execution

---

# 📌 Exception Hierarchy

```
                    Object
                       │
                  Throwable
                 /         \
             Error       Exception
                            │
          ┌─────────────────┴─────────────────┐
          │                                   │
 Checked Exceptions               RuntimeException
                                              │
                                  Unchecked Exceptions
                                              │
                     ┌──────────────┬──────────────┐
                     │              │              │
          ArithmeticException   NullPointerException
          ArrayIndexOutOfBoundsException
```

---

# 📌 Error vs Exception

| Error | Exception |
|--------|-----------|
| Serious JVM/System problem | Application problem |
| Usually cannot be handled | Can be handled |
| Example: OutOfMemoryError | Example: IOException |

---

# 📌 try - catch - finally

## try

Contains **risky code**.

```java
try{

}
```

---

## catch

Handles the exception.

```java
catch(Exception e){

}
```

---

## finally

Always executes.

Used for **resource cleanup**.

```java
finally{

}
```

---

# 🧠 Flow

```
try

↓

Exception?

↓

Yes → catch

↓

finally

-----------------------

No Exception

↓

Skip catch

↓

finally
```

---

# 📌 throw vs throws

## throw

Actually throws an exception.

```java
throw new ArithmeticException();
```

---

## throws

Declares that a method **may throw** an exception.

```java
void readFile() throws IOException{

}
```

---

# 📊 throw vs throws

| throw | throws |
|--------|---------|
| Actually throws exception | Declares exception |
| Used inside method | Used in method signature |
| One exception at a time | Can declare multiple exceptions |

---

# 📌 Checked vs Unchecked Exception

## Checked Exception

- Compiler checks
- Must handle
- Compile-time

Examples

```
IOException

SQLException

FileNotFoundException
```

---

## Unchecked Exception

- JVM checks
- Runtime
- Optional to handle

Examples

```
ArithmeticException

NullPointerException

ArrayIndexOutOfBoundsException

NumberFormatException
```

---

# 📊 Checked vs Unchecked

| Checked | Unchecked |
|----------|-----------|
| Compiler checks | JVM checks |
| Must handle | Optional |
| Compile Time | Runtime |
| IOException | ArithmeticException |

---

# 📌 final vs finally vs finalize()

| final | finally | finalize() |
|--------|----------|-------------|
| Cannot modify | Always executes | Called by Garbage Collector (Deprecated) |
| Variable/Method/Class | Block | Method |

---

# 📌 Multiple Catch Blocks

✅ Allowed

```java
try{

}
catch(IOException e){

}
catch(Exception e){

}
```

Always write

```
Specific Exception

↓

General Exception
```

---

# 📌 Features

| Feature | Purpose |
|----------|----------|
| try | Risky code |
| catch | Handle exception |
| finally | Cleanup |
| throw | Throw exception |
| throws | Declare exception |

---

# 🧠 Mind Map

```text
               Exception Handling

                        │

       Handle Runtime Errors

                        │

     ┌──────────┬──────────┬──────────┐
     │          │          │          │
    try       catch     finally    throw
     │          │          │          │
Risky Code  Handle     Cleanup   Throw Exception

                        │

                    throws

                        │

                 Declare Exception

                        │

      ┌─────────────────┴────────────────┐
      │                                  │
 Checked Exception              Unchecked Exception
      │                                  │
 Compiler Checks                Runtime Checks
```

---

# 💡 Memory Tricks

### Trick 1

```
try

↓

Risky Code
```

---

### Trick 2

```
catch

↓

Handle Error
```

---

### Trick 3

```
finally

↓

Always Executes

↓

Cleanup
```

---

### Trick 4

```
throw

↓

Actually Throws

--------------------

throws

↓

May Throw
```

---

### Trick 5

```
RuntimeException

↓

Unchecked

Everything Else

↓

Checked
```

---

# 🚨 Interview Traps

### Can try exist without catch?

✅ Yes

If finally is present.

---

### Can catch exist without try?

❌ No

---

### Can finally execute without exception?

✅ Yes

Always.

---

### Can multiple catch blocks exist?

✅ Yes

---

### Which executes always?

```
finally
```

---

# ⭐ Most Asked Interview Questions

| Question | Answer |
|----------|--------|
| What is Exception Handling? | Handle runtime errors |
| Why use it? | Prevent program crash |
| Difference between Error & Exception? | Error → JVM, Exception → Application |
| Checked Exception? | Compiler checks |
| Unchecked Exception? | Runtime checks |
| Difference between throw & throws? | Throw → action, Throws → declaration |
| Difference between final, finally, finalize()? | Keyword, Block, Method |
| Which block always executes? | finally |

---

# ⚡ 30-Second Revision

```
Exception Handling

↓

Handle Runtime Errors

↓

try

↓

catch

↓

finally

↓

throw

↓

throws

↓

Checked

↓

Unchecked
```

---

# ⚡ 5-Second Revision

```
try

↓

catch

↓

finally

↓

throw

↓

throws

↓

Checked

↓

Unchecked
```