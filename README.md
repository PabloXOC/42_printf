# 42 ft_printf

The `ft_printf` project implements a custom version of the `printf` function from the C standard library. This function mimics the behavior of the original `printf` while offering a variety of format specifiers for printing characters, strings, numbers, and more. This project enhances understanding of variadic functions, memory management, and formatted output in C.

---

## Features

- **Format Specifiers**: Handles the following format specifiers:
  - `%c`: Prints a single character.
  - `%s`: Prints a string.
  - `%p`: Prints a pointer in hexadecimal format.
  - `%d`: Prints a signed decimal (base 10) number.
  - `%i`: Prints an integer in base 10.
  - `%u`: Prints an unsigned decimal (base 10) number.
  - `%x`: Prints a number in hexadecimal (lowercase).
  - `%X`: Prints a number in hexadecimal (uppercase).
  - `%%`: Prints a percent sign.

- **Variadic Arguments**: Uses `va_start`, `va_arg`, and `va_end` to handle a variable number of arguments, allowing flexibility in the input.

- **Library Creation**: The library is compiled into `libftprintf.a`, providing a reusable function for formatted output.

---

## Project Files

- **`ft_printf.c`**: Contains the main implementation of the `ft_printf` function.
- **`ft_printf_utils.c`**: Includes helper functions used by `ft_printf`, such as handling different format specifiers.
- **`ft_printf.h`**: Header file with function prototypes and necessary includes.
- **`Makefile`**: Contains the build instructions for compiling the library.

---

## Function Prototype

```c
int ft_printf(const char *format, ...);
```

### Parameters
- **`format`**: The format string, which may contain the following specifiers: `c`, `s`, `p`, `d`, `i`, `u`, `x`, `X`, `%%`.

### Return Value
- **`int`**: The number of characters printed (excluding the null byte).

---

## Compilation Instructions

To compile the code, use the following command:

```bash
make
```

This will compile the library into `libftprintf.a` and create the object files. You can use the library in your projects by linking to it when compiling your code.

To clean the project files, use:

```bash
make clean
```

To remove object files and the compiled library, use:

```bash
make fclean
```

To rebuild the library from scratch, use:

```bash
make re
```

---

## Usage Example

Here’s an example of using `ft_printf`:

```c
#include "ft_printf.h"

int main(void)
{
    int n = 42;
    ft_printf("Hello, world!\n");
    ft_printf("Decimal: %d, Hex: %x\n", n, n);
    return 0;
}
```

---

## Key Considerations

- **No Buffer Management**: Unlike the original `printf`, `ft_printf` does not implement buffer management.
- **Specifiers Supported**: Handles common format specifiers, including character, string, pointer, integer, unsigned, and hexadecimal.
- **Memory Management**: Utilizes `malloc` and `free` as necessary for dynamic memory allocation.
- **Error Handling**: Returns the number of characters printed, or an error code if something goes wrong.

---

## Learnings and Reflections

This project provided valuable insights into:
- **Variadic Functions**: Working with variable arguments using `va_start`, `va_arg`, and `va_end`.
- **Formatted Output**: Understanding how to parse format strings and convert data types into appropriate string representations.
- **Library Creation**: Building a reusable C library and mastering the `ar` tool for creating static libraries.

By implementing `ft_printf`, I have developed a deeper understanding of how formatted output functions work at a low level, which will be useful for more complex system-level programming tasks.

---

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).
```

This README provides a comprehensive but concise explanation of the `ft_printf` project, highlighting its features, usage, and the lessons learned from implementing it. It ensures that users can easily understand how to use the function and the purpose of the project. Let me know if you need any changes!
