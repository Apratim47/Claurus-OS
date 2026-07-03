
# CS50x Week 1

## Status

🚧 In Progress

---

# Linux Commands

| Command | Purpose |
|----------|---------|
| `ls` | List files and directories |
| `mkdir` | Create a new directory |
| `rm` | Remove a file |
| `mv` | Move or rename files/directories |
| `cp` | Copy files/directories |
| `cd` | Change the current directory |
| `pwd` | Display the current working directory |

---

# Writing a C Program

```c
#include <stdio.h>

int main(void)
{
    printf("hello, world\n");
}
```

## Learned

- `#include <stdio.h>` includes the Standard Input/Output library.
- `main()` is the entry point of every C program.
- Curly braces `{}` define the function body.
- Every statement ends with a semicolon `;`.
- `printf()` is used to display output.

---

# Compilation & Execution

```bash
code hello.c
make hello
./hello
```

## Learned

- `code hello.c` → Opens the file in Visual Studio Code.
- `make hello` → Compiles `hello.c` into an executable named `hello`.
- `./hello` → Runs the compiled program.

---

# Data Types

- `int` → Integer
- `float` → Floating-point number
- `double` → Double-precision floating-point number
- `char` → Single character
- `bool` → Boolean value (true/false)
- `string` → Sequence of characters (provided by the CS50 Library)

---

# Operators

## Arithmetic Operators

- `+` Addition
- `-` Subtraction
- `*` Multiplication
- `/` Division
- `%` Modulus (Remainder)

## Comparison Operators

- `==` Equal to
- `!=` Not equal to
- `<` Less than
- `>` Greater than
- `<=` Less than or equal to
- `>=` Greater than or equal to

## Logical Operators

- `&&` Logical AND
- `||` Logical OR
- `!` Logical NOT

---

# Conditions

Conditional statements allow a program to make decisions.

- `if`
- `else`
- `else if`

Example:

```c
if (x > 0)
{
    printf("Positive\n");
}
```

---

# Format Specifiers

| Specifier | Meaning |
|------------|---------|
| `%i` | Integer |
| `%d` | Integer |
| `%f` | Floating-point number |
| `%c` | Character |
| `%s` | String |

---

# Escape Characters

| Escape Character | Meaning |
|------------------|---------|
| `\n` | New line |
| `\"` | Double quotation mark |
| `\\` | Backslash |

---

# Important Concepts

- Source Code
- Compiler
- Executable
- Function
- Library
- Header File
- Terminal

---

# Commands Learned

```bash
code hello.c
make hello
./hello
```

---

# My Takeaways

- Learned the basic structure of a C program.
- Understood how to compile and run C programs.
- Learned essential Linux terminal commands.
- Learned basic data types, operators, and conditions.
- Learned how format specifiers and escape characters work.

---

# Things to Revise

- Difference between `int`, `float`, and `double`
- More practice with Linux commands
- More practice with operators and conditions

---

# Questions

- How does the compiler convert C code into machine code?
- What happens internally when `make` is executed?
- How does `printf()` work behind the scenes?
