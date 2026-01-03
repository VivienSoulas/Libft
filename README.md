# libft - A Custom C Standard Library

A from-scratch implementation of essential C standard library functions, demonstrating deep understanding of memory management, string manipulation, and data structures.

## Overview

libft is a foundational project that recreates core functionality from the C standard library (`libc`). Rather than using pre-built functions, every implementation is written from first principles, revealing how these seemingly simple utilities actually work under the hood.

This project bridges the gap between "how to use a function" and "how a function actually works"—a critical distinction for systems programming and optimization.

## Core Components

### String & Character Functions
Functions like `ft_strlen`, `ft_strcpy`, and `ft_substr` handle text manipulation and memory safety. Each implementation reveals common pitfalls:
- Buffer overflow prevention
- Null-terminator handling
- Edge case management (empty strings, overlapping memory)

These basics are used in nearly every C project, making them essential knowledge for any systems programmer.

### Memory Management
Functions like `ft_memcpy`, `ft_memmove`, and `ft_calloc` manage raw memory operations. Understanding these is crucial because:
- `ft_memmove` handles overlapping memory regions safely—a classic challenge
- `ft_calloc` combines allocation with initialization
- Memory operations must be efficient since they're called frequently

This section reveals why certain functions exist and why you can't always safely substitute one for another.

### List Functions (Bonus)
Bonus functions implement a singly-linked list abstraction with operations like `ft_lstadd_back`, `ft_lstiter`, and `ft_lstmap`. This demonstrates:
- Dynamic data structure design
- Function pointers for generic operations
- Memory responsibility and cleanup

### Utility Functions
Conversion functions like `ft_atoi` and `ft_itoa` transform between data types. String splitting (`ft_split`), character checking (`ft_isalpha`, `ft_isdigit`), and character class classification all require careful input validation.

## Why This Matters

Building libft teaches fundamental programming principles:
- **Precision**: Even "simple" functions have edge cases that must be handled correctly
- **Efficiency**: Memory operations must be optimized since they're called millions of times
- **Responsibility**: Whoever writes a utility function is responsible for its correctness everywhere it's used
- **Documentation**: Without an external library to reference, clear thinking about intent becomes critical

## Building

```bash
make          # Compile the library
make clean    # Remove object files
make fclean   # Remove library and objects
make re       # Rebuild
```

This produces `libft.a`, a static library ready to link with other projects.

## Learning Outcomes

This project is about mastering the fundamentals. It demonstrates:
- **Buffer safety**: Understanding why certain functions exist
- **Memory efficiency**: Why optimized string operations matter
- **Attention to detail**: Small bugs in utility functions cascade through entire systems
- **Standard compliance**: How to match POSIX behavior and edge case handling

---

*A 42 School project showcasing C fundamentals and systems programming principles.*
