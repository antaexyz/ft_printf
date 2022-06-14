# ft_printf

### Introduction

This is the third project at 42 programming school. We had to create a static library that contains `ft_printf` a function that mimics the real printf. The printf function is one of the most known and used in the C language to give an output. It takes a string as an argument, this string may contain some placeholders (like %c for characters or %s for strings) whose original values are passed as arguments. The ft_printf has variable arguments, the only one being mandatory is the string that will be printed. To create a function like this, we had to understand how the variadic functions work. The function returns the number of characters printed or -1 for error.

✨ *Full subject [here](https://drive.google.com/file/d/1Ut8UDWIrN7HXHVPOqItnPsayUe8HsSzD/view?usp=sharing) ✨*

My ft_printf supports all these converters, flags and modifiers:

| Converter | Description            |
| --------- | ---------------------- |
| s         | ascii strings          |
| S         | unicode strings        |
| p         | pointers               |
| c         | ascii character        |
| C         | unicode character      |
| x X       | hexadecimal conversion |
| u U       | unsigned decimal       |
| o O       | octal conversion       |
| i d D     | signed decimal         |
| %%        | print a percent sign   |

| Flag | Description                               |
| ---- | ----------------------------------------- |
| #    | add '0x' for hexadecimal or '0' for octal |
| 0    | complete the indicated width with zeros   |
| -    | apply width after the argument            |
| +    | add '+' sign for positive numbers         |

| Modifier | Description                                         |
| -------- | --------------------------------------------------- |
| hh       | cast the argument in char / unsigned char           |
| h        | cast the argument in short / unsigned short         |
| l        | cast the argument in long / unsigned long           |
| ll       | cast the argument in long long / unsigned long long |


### Allowed functions

```bash
malloc, free, write, va_start, va_arg, va_copy, va_end
```

### Usage

**1 - Clone this repo**

```bash
git https://github.com/antae16/ft_printf.git
cd ft_printf
```

**2 - Build the library**

```bash
make
```

You should see a `libftprinf.a`  file and obj folder that contains some object files (.o)

**3 - Compile your project with the library**

```bash
gcc -Wall -Wextra -Werror -I [ft_printf_path/headers] [your_file.c] [ft_printf_path/ft_printf.a]
```

(don’t forget to include `ft_printf.h` in your project)

### Ressources

[https://linux.die.net/man/3/printf](https://linux.die.net/man/3/printf)

[https://www.tutorialspoint.com/c_standard_library/c_macro_va_arg.htm](https://www.tutorialspoint.com/c_standard_library/c_macro_va_arg.htm)

### If you are wondering why we don't use many built-in functions and for loops)

[The Norm](https://github.com/42School/norminette) is our school coding guidelines for all programs written in C. A single Norm Error leads to the grade of 0/100. Here are some of the rules to follow :

- forbidden functions: almost all the Standard C Library functions except read, open, write, malloc and free for some projects
- 25 lines per function maximum (without external brackets) and 84 characters per line maximum
- no more than 5 functions in a .c file and no more than 5 variables per function, no comments within a function's body
- for loops are forbidden
