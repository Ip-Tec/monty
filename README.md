# Monty Project README

## Overview
Welcome to the Monty project, a team-based endeavor in C programming focusing on stacks and queues, LIFO, FIFO. This project aims to build an interpreter for Monty ByteCodes files, creating a scripting language compiled into Monty byte codes.

## Team Information
- **Project Name:** Monty
- **Team Members:** Ip

## Project Timeline
- **Project Start:** December 12, 2023, 6:00 AM
- **Project Deadline:** December 18, 2023, 6:00 AM
- **Auto QA Review:** Pending (Scheduled for deadline)

## Project Objectives
The primary objectives of this project include understanding and implementing the following concepts:
- Stacks and Queues in C
- Stack and Queue operations
- LIFO (Last In, First Out) and FIFO (First In, First Out)
- Proper use of global variables
- Handling external variables using `extern` in C
- Implementing algorithms and data structures
- Learning and applying the Betty style for C programming
- Understanding and implementing push, pall, pint, pop, swap, add, nop, sub, div, mul, mod, comments, pchar, pstr, rotl, rotr, stack, and queue opcodes.

## Project Requirements
1. **Allowed Editors:** vi, vim, emacs
2. **Compilation:** Ubuntu 20.04 LTS, gcc with options -Wall -Werror -Wextra -pedantic -std=c89
3. **File Structure:** All files should end with a newline, include a README.md file, adhere to the Betty style, and have a maximum of one global variable.
4. **Functions:** No more than 5 functions per file. Prototypes should be in the header file `monty.h`.
5. **Version Control:** One project repository per group. Clone/fork cautiously to avoid scoring issues.

## Data Structures
Please use the following data structures in your project:
```c
typedef struct stack_s
{
        int n;
        struct stack_s *prev;
        struct stack_s *next;
} stack_t;

typedef struct instruction_s
{
        char *opcode;
        void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;
```
## Compilation & Output
Compile the code using:

```bash
$ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
```
Print output on stdout and error messages on stderr.

## Running the Monty Program
Usage:
```bash
$ ./monty file
```

- If no file or more than one argument is given, print USAGE: monty file and exit with EXIT_FAILURE.
- If the file cannot be opened, print Error: Can't open file <file> and exit with EXIT_FAILURE.
- If an invalid instruction is encountered, print L<line_number>: unknown instruction <opcode> and exit with EXIT_FAILURE.
- If malloc fails, print Error: malloc failed and exit with EXIT_FAILURE.

