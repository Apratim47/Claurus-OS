# CS50x Week 2 - Arrays, Strings & Debugging

## Status
✅ Completed

---

# Topics Covered

- Reading Levels
- Cryptography
- Debugging
- Arrays
- Strings
- Characters
- Command Line Arguments
- Compiler Internals
- Header Files
- Libraries
- Function Prototypes

---

# Reading Levels

A computer can determine the reading difficulty of a paragraph by analyzing:

- Number of letters
- Number of words
- Number of sentences

This idea is used in the Week 2 problem set.

---

# Cryptography

Cryptography is the process of protecting information by converting readable text into an unreadable form.

Important terms:

- Plaintext → Original message
- Ciphertext → Encrypted message
- Encryption → Converting plaintext into ciphertext
- Decryption → Converting ciphertext back to plaintext

Purpose:
- Secure communication
- Password protection
- Online banking
- HTTPS
- Messaging apps

---

# Debugging

A bug is an error in a program.

Debugging means finding and fixing bugs.

Types of bugs:

## 1. Syntax Error

The code does not compile.

Example:
- Missing semicolon
- Missing braces
- Misspelled keyword

---

## 2. Logic Error

The program compiles but produces the wrong result.

Example:

```
2 + 2 = 5
```

The compiler cannot detect logical mistakes.

---

# Debugging Techniques

- Read compiler errors carefully.
- Use printf() to inspect variables.
- Use debug50.
- Explain your code to a rubber duck (Rubber Duck Debugging).
- Ask AI only after trying yourself.

> Learn to solve problems first instead of depending completely on AI.

---

# Arrays

An array stores multiple values of the same type.

Example:

```c
int scores[3];
```

Instead of:

```c
int score1;
int score2;
int score3;
```

Arrays are cleaner and easier to manage.

---

# Array Indexing

Arrays start from index 0.

Example:

```text
Index : 0 1 2
Value : A B C
```

Access:

```c
letters[0]
letters[1]
letters[2]
```

---

# Characters vs Strings

Character:

```c
'A'
```

Uses single quotes.

String:

```c
"Apple"
```

Uses double quotes.

A string is simply an array of characters ending with the null character (`'\0'`).

---

# Strings

Strings can be accessed one character at a time.

Example:

```c
string name = "David";

name[0] = D
name[1] = a
name[2] = v
...
```

This allows programs to inspect and modify text.

---

# string.h Library

Useful functions:

```c
strlen()
```

Returns the length of a string.

Example:

```c
strlen("Hello")
```

returns

```
5
```

---

# ctype.h Library

Useful functions:

```c
toupper()
tolower()
islower()
isupper()
```

Instead of writing your own conversion logic, use library functions whenever possible.

---

# Why Libraries Matter

Libraries save time.

Instead of solving common problems yourself, use tested functions written by other programmers.

Example:

- printf()
- strlen()
- toupper()

---

# Header Files

Header files tell the compiler which functions exist.

Example:

```c
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#include <cs50.h>
```

Without the correct header, the compiler does not know about the function.

---

# Function Prototype

A prototype tells the compiler:

- Function name
- Inputs
- Return type

Example:

```c
int square(int n);
```

The actual implementation can appear later in the file.

---

# Command Line Arguments

Until now:

```c
int main(void)
```

takes no input from the terminal.

Now:

```c
int main(int argc, string argv[])
```

allows input while running the program.

Example:

```
./greet David
```

Here:

```
argc = 2
argv[0] = "./greet"
argv[1] = "David"
```

Useful for programs that accept user input directly from the terminal.

---

# Compiler Process

When running:

```
make hello
```

Several steps happen internally.

## 1. Preprocessing

Copies the contents of header files.

```
#include <stdio.h>
```

↓

Compiler inserts function prototypes.

---

## 2. Compiling

Converts C code into Assembly language.

---

## 3. Assembling

Converts Assembly into Machine Code (0s and 1s).

---

## 4. Linking

Combines:

- Your code
- Standard Library
- CS50 Library

into one executable program.

---

# make vs clang

`clang`

- Actual compiler
- More control
- Longer commands

Example:

```
clang hello.c -lcs50 -o hello
```

`make`

- Automatically runs the correct compiler commands.
- Easier to use.

Example:

```
make hello
```

---

# Design Principle

If a function already exists,

**use it instead of reinventing it.**

Example:

Instead of writing your own uppercase conversion,

use

```c
toupper()
```

---

# Key Takeaways

- Arrays organize data efficiently.
- Strings are arrays of characters.
- Libraries prevent unnecessary work.
- Header files expose function prototypes.
- Debugging is an essential programming skill.
- Learn to interpret compiler errors.
- Programs can receive command-line arguments.
- Compilation consists of:
  - Preprocessing
  - Compiling
  - Assembling
  - Linking
- `make` simplifies compilation.
- Good programmers reuse existing tools instead of rewriting everything.
