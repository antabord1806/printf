# ft_printf

<div align="center">
  <h1>📝 ft_printf</h1>
  <p><strong>Because ft_putnbr() and ft_putstr() aren't enough</strong></p>
  
  ![42 School Badge](https://img.shields.io/badge/42-Project-00babc?style=flat-square&logo=42)
  ![Language](https://img.shields.io/badge/Language-C-blue?style=flat-square)
  ![Norminette](https://img.shields.io/badge/Norminette-passing-success?style=flat-square)
</div>

---

## 📋 Table of Contents
- [About](#about)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Function Prototype](#function-prototype)
- [Supported Conversions](#supported-conversions)
- [Return Value](#return-value)
- [Examples](#examples)
- [Project Structure](#project-structure)
- [Testing](#testing)
- [Resources](#resources)
- [Author](#author)
- [License](#license)

---

## 📖 About

**ft_printf** is a 42 School project that recreates the famous `printf()` function from the C standard library. This project aims to deepen understanding of variadic functions and improve programming skills by implementing a complex and highly useful C function from scratch.

The goal is to recode the `printf()` function from libc, learning about:
- Variadic functions in C
- String parsing and formatting
- Type conversions
- Memory management
- Edge case handling

**Grade**: 🎯 (In progress)

---

## ✨ Features

- ✅ Handles multiple conversion specifiers
- ✅ Supports flags, width, and precision
- ✅ Compatible with original printf behavior
- ✅ Efficient memory management
- ✅ Follows 42 School Norminette coding standards
- ✅ No memory leaks

---

## 🔧 Requirements

- **Operating System**: Linux / macOS
- **Compiler**: gcc or clang
- **Make**: GNU Make
- **Language Standard**: C (C99 or later)

---

## 🚀 Installation

Clone the repository and compile the project:

```bash
# Clone the repository
git clone https://github.com/antabord1806/printf.git

# Navigate to the project directory
cd printf

# Compile the library
make

# This will generate the libftprintf.a static library
```

---

## 💻 Usage

Include the header in your C file and compile with the library:

```c
#include "ft_printf.h"

int main(void)
{
    ft_printf("Hello, %s!\n", "world");
    ft_printf("Number: %d\n", 42);
    ft_printf("Hex: %x\n", 255);
    return (0);
}
```

Compile your program:

```bash
gcc -Wall -Wextra -Werror your_file.c -L. -lftprintf -o your_program
```

---

## 📝 Function Prototype

```c
int ft_printf(const char *format, ...);
```

---

## 🎨 Supported Conversions

The function handles the following conversion specifiers:

| Specifier | Description | Example |
|-----------|-------------|---------|
| `%c` | Character | `ft_printf("%c", 'A')` → A |
| `%s` | String | `ft_printf("%s", "hello")` → hello |
| `%p` | Pointer address | `ft_printf("%p", ptr)` → 0x7ffd5e8a9c60 |
| `%d` | Signed decimal integer | `ft_printf("%d", -42)` → -42 |
| `%i` | Signed decimal integer | `ft_printf("%i", 42)` → 42 |
| `%u` | Unsigned decimal integer | `ft_printf("%u", 42)` → 42 |
| `%x` | Hexadecimal lowercase | `ft_printf("%x", 255)` → ff |
| `%X` | Hexadecimal uppercase | `ft_printf("%X", 255)` → FF |
| `%%` | Percent sign | `ft_printf("%%")` → % |

### Additional Flags (Bonus)

- `-` : Left-justify within the given field width
- `0` : Zero-padding for numeric conversions
- `.` : Precision specification
- `#` : Alternative form
- ` ` : Space before positive numbers
- `+` : Sign always printed for signed conversions
- Minimum field width

---

## 📤 Return Value

Returns the number of characters printed (excluding the null byte used to end output to strings). Returns -1 on error.

---

## 📚 Examples

```c
#include "ft_printf.h"

int main(void)
{
    int len;
    
    // Basic string printing
    len = ft_printf("Hello, World!\n");
    ft_printf("Characters printed: %d\n", len);
    
    // Number formatting
    ft_printf("Decimal: %d\n", 42);
    ft_printf("Unsigned: %u\n", 42);
    ft_printf("Hexadecimal: %x\n", 255);
    ft_printf("Uppercase Hex: %X\n", 255);
    
    // Pointer printing
    int *ptr = &len;
    ft_printf("Pointer: %p\n", ptr);
    
    // Character printing
    ft_printf("Char: %c\n", 'A');
    
    // Mixed formatting
    ft_printf("String: %s, Number: %d, Hex: %x\n", "test", 100, 100);
    
    // Percent sign
    ft_printf("100%% complete\n");
    
    return (0);
}
```

---

## 📁 Project Structure

```
printf/
├── README.md           # Project documentation
├── Makefile           # Compilation rules
├── ft_printf.h        # Header file with prototypes
├── ft_printf.c        # Main function implementation
├── ft_print_char.c    # Character printing functions
├── ft_print_str.c     # String printing functions
├── ft_print_ptr.c     # Pointer printing functions
├── ft_print_nbr.c     # Number printing functions
├── ft_print_hex.c     # Hexadecimal printing functions
└── ft_print_utils.c   # Utility functions
```

---

## 🧪 Testing

To test the ft_printf function:

```bash
# Compile with main test file
gcc -Wall -Wextra -Werror main.c -L. -lftprintf -o test

# Run tests
./test

# Compare with original printf
./test > your_output.txt
# Compare outputs manually or with diff tools
```

### Recommended Testers

- [printfTester](https://github.com/Tripouille/printfTester)
- [ft_printf_tester](https://github.com/paulo-santana/ft_printf_tester)
- [42TESTERS-PRINTF](https://github.com/xicodomingues/francinette)

---

## 📚 Resources

### Variadic Functions
- [stdarg.h documentation](https://en.cppreference.com/w/c/variadic)
- [Variadic functions in C](https://www.gnu.org/software/libc/manual/html_node/Variadic-Functions.html)

### Printf Reference
- [printf man page](https://man7.org/linux/man-pages/man3/printf.3.html)
- [printf format string](https://en.wikipedia.org/wiki/Printf_format_string)

### 42 School
- [42 Cursus](https://42.fr/en/homepage/)
- [42 Network](https://www.42network.org/)

---

## 👤 Author

**antabord1806**

- GitHub: [@antabord1806](https://github.com/antabord1806)
- 42 Intra: `antabord`

---

## 📄 License

This project is part of the 42 School curriculum. Feel free to use it for educational purposes.

---

<div align="center">
  <p>Made with ❤️ at 42 School</p>
  <p>⭐ Star this repository if you found it helpful!</p>
</div>