# C Programming: Topics & Code Snippets

| **#** | **Topic**                | **Subtopics / Examples** |
|------|---------------------------|---------------------------|
| 1    | Introduction to C         | History, Structure, Compilation, Execution |
| 2    | Data Types & Variables    | int, float, char, double, constants, type modifiers |
| 3    | Operators                 | Arithmetic, Logical, Relational, Bitwise, Assignment, Ternary |
| 4    | Control Structures        | if-else, switch, for, while, do-while, break, continue, goto |
| 5    | Functions                 | Declaration, Definition, Arguments, Return, Recursion |
| 6    | Arrays                    | 1D, 2D, manipulation, sorting, searching |
| 7    | Strings                   | String functions (`strlen`, `strcpy`, `strcat`), input/output |
| 8    | Pointers                  | Basics, Arithmetic, Arrays, Functions, Double pointers |
| 9    | Structures & Unions       | Structure, nested structures, unions, differences |
| 10   | Dynamic Memory Allocation | malloc, calloc, realloc, free |
| 11   | File Handling             | fopen, fclose, fread, fwrite, fgetc, fputc, fscanf, fprintf |
| 12   | Preprocessor Directives   | `#define`, `#include`, `#ifdef`, `#ifndef` |
| 13   | Command Line Arguments    | argc, argv usage |
| 14   | Linked Lists              | Singly Linked List, insertion, deletion |
| 15   | Miscellaneous             | Enum, Typedef, `errno` |

---

## Code Examples

| **Title**       | **Code Snippet** |
|----------------|------------------|
| Hello World    | ```c<br>#include <stdio.h><br>int main() { printf("Hello, World!"); return 0; }<br>``` |
| Factorial      | ```c<br>int factorial(int n) { if (n == 0) return 1; return n * factorial(n - 1); }<br>``` |
| Pointer Usage  | ```c<br>int x = 10; int *p = &x; printf("%d", *p);<br>``` |
| Structure Demo | ```c<br>struct student { char name[20]; int age; };<br>``` |
|Link list| [Chake out](code.md#link-list)|
