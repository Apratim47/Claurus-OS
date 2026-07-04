
# CS50x Week 1 - C

## Status

✅ Completed

---

# Overview

This week introduced the C programming language and how programs are compiled and executed. Although C requires more work than Scratch, it provides much greater control over how programs interact with the computer.

---

# Linux Terminal Commands

| Command | Purpose |
|----------|---------|
| `ls` | List files and directories |
| `pwd` | Show the current working directory |
| `cd` | Change directory |
| `mkdir` | Create a directory |
| `cp` | Copy files or directories |
| `mv` | Move or rename files/directories |
| `rm` | Remove files |
| `code file.c` | Open a file in VS Code |

---

# Basic Structure of a C Program

```c
#include <stdio.h>

int main(void)
{
    printf("Hello, world!\n");
}
```

## Explanation

### `#include <stdio.h>`

Imports the Standard Input/Output library.

Without it, functions like `printf()` cannot be used.

---

### `int main(void)`

Every C program starts execution here.

- `int` → The function returns an integer.
- `main` → The entry point of the program.
- `void` → No arguments are passed into the program.

---

### Curly Braces `{ }`

Everything inside these braces belongs to the function.

---

### Semicolon `;`

Almost every statement in C ends with a semicolon.

---

# printf()

Used to display output on the screen.

Example:

```c
printf("Hello!\n");
```

---

# Escape Characters

| Escape Character | Meaning |
|------------------|---------|
| `\n` | New line |
| `\"` | Double quotation mark |
| `\\` | Backslash |

---

# Compilation

Source code cannot run directly.

Process:

```
hello.c
      ↓
Compiler
      ↓
Machine Code
      ↓
Executable Program
```

---

# Commands Used

```bash
code hello.c
make hello
./hello
```

### Meaning

`code hello.c`

Open the file in VS Code.

---

`make hello`

Compile `hello.c`.

Equivalent to using a compiler manually, but easier.

---

`./hello`

Run the compiled program.

---

# Data Types

## int

Stores integers.

Example:

```c
int age = 18;
```

---

## float

Stores decimal numbers.

Example:

```c
float pi = 3.14;
```

---

## double

Stores decimal numbers with higher precision than float.

---

## char

Stores one character.

Example:

```c
char grade = 'A';
```

---

## bool

Stores either:

- true
- false

---

## string (CS50 Library)

Stores text.

Example:

```c
string name = "Apratim";
```

Internally, a string is a sequence of characters.

---

# Variables

Variables store information.

Example:

```c
int score = 100;
```

Think of a variable as a labeled box that stores data.

---

# Operators

## Arithmetic

| Operator | Meaning |
|----------|---------|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Remainder |

---

## Comparison

| Operator | Meaning |
|----------|---------|
| == | Equal |
| != | Not Equal |
| < | Less Than |
| > | Greater Than |
| <= | Less Than or Equal |
| >= | Greater Than or Equal |

---

## Logical

| Operator | Meaning |
|----------|---------|
| && | AND |
| \|\| | OR |
| ! | NOT |

---

# Conditions

Used to make decisions.

Example:

```c
if (score >= 50)
{
    printf("Pass\n");
}
else
{
    printf("Fail\n");
}
```

---

# Format Specifiers

Used with `printf()`.

| Specifier | Meaning |
|-----------|---------|
| `%i` | Integer |
| `%d` | Integer |
| `%f` | Float |
| `%c` | Character |
| `%s` | String |

Example:

```c
printf("%i\n", age);
```

---

# User Input

CS50 provides helper functions.

Example:

```c
int age = get_int("Age: ");
```

Other functions include:

- `get_char()`
- `get_float()`
- `get_double()`
- `get_string()`

---

# Functions

A function performs a specific task.

Example:

```c
printf("Hello");
```

`printf()` is a function.

---

## Why Functions?

Instead of repeating code:

```c
printf("#\n");
printf("#\n");
printf("#\n");
```

Create one function and call it multiple times.

Functions make programs:

- Cleaner
- Easier to maintain
- Easier to reuse

---

# Function Prototype

Sometimes you call a function before defining it.

Example:

```c
void meow(void);

int main(void)
{
    meow();
}

void meow(void)
{
    printf("Meow\n");
}
```

The line

```c
void meow(void);
```

is called a **function prototype**.

It tells the compiler:

> "This function exists. Its full definition will appear later."

Without a prototype, the compiler may produce an error.

---

# Loops

## for Loop

Used when the number of repetitions is known.

Example:

```c
for (int i = 0; i < 3; i++)
{
    printf("Hello\n");
}
```

---

## while Loop

Runs while a condition remains true.

Example:

```c
while (true)
{
    printf("Running\n");
}
```

---

# Common Programming Workflow

```
Write Code
      ↓
Compile
      ↓
Fix Errors
      ↓
Run Program
      ↓
Improve Code
```

---

# Important Terms

### Source Code

Human-readable code.

---

### Compiler

Converts source code into machine code.

---

### Machine Code

Instructions understood by the CPU.

---

### Executable

The compiled program that can be run.

---

### Library

A collection of useful functions.

---

### Header File

Declares functions available in a library.

Example:

```c
#include <stdio.h>
```

---

# Things I Learned

- How C programs are structured.
- Why libraries are needed.
- How compilation works.
- How to use Linux terminal commands.
- Variables and data types.
- Arithmetic, comparison, and logical operators.
- Conditions and loops.
- Functions.
- Function prototypes.
- Basic program organization.

---

# Things to Revise

- Function prototypes
- Loops
- Operators
- Data types
- Format specifiers

---

# Questions for Future Me

- How does `make` actually compile a program?
- How does the compiler find header files?
- How are strings stored in memory?
- What happens inside `printf()`?
- How does the CPU execute machine code?

---

# Relation to Claurus OS

Everything learned this week forms the foundation for operating system development.

Understanding C is essential because operating systems rely heavily on:

- Functions
- Memory
- Variables
- Program structure
- Compilation
- Interaction with hardware

These concepts will be used repeatedly while building Claurus OS.
