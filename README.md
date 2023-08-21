  **ALX Africa – Holberton Software Engineering Program’s Printf Group Project.**

This Readme file is for a group project, handled by my partner; Chioma Victor and I; Immaculata Etukenyin. It is a custom made printf function for the C programming language called _printf that requires writing codes for functions, flags, presicion, size, width, utils, handlers, a test file and prototypes in main.h files. It takes in various inputs and optional arguments based exactly on how the standard library function printf works. My partner and I, submitted this as our first group project for grading as part of our ALX software engineering course requirement.

**OUTLINE**

**The _printf() function** is a function that produces output according to a given format without making use of the standard library files. It uses a local buffer of 1024 chars in order to call write as little as possible. The printf function handles the custom conversion specifier, the flag characters and length modifiers for non-custom conversion specifiers. The _printf() function returns the total number of characters printed to the stdout(excluding the null byte at the end of strings) after a successful execution.

**The prototype int _printf(const char format, ...);** was used, This prototype tells us that the "printf" function takes two arguments: a format string and a variable number of arguments.
The **"..." indicates** that the number of arguments is variable. The **"const char format" indicates** that the first argument is a constant character string that's used to determine how the other arguments are printed. The second argument is a list of additional arguments that are printed according to the format string. So, the "printf" function takes two arguments: a format string and a variable number of other arguments. The printf function takes a format string as an argument, which specifies the layout of the output. The function then iterates through the format string, interpreting the format specifiers and producing output based on them.

**The Format Specifiers** 
The format specifiers are characters that begin with a percentage sign (%) and are used to control the output format. There are three different types of format specifiers: string format specifiers, integer format specifiers, and floating-point format specifiers.

**Integer format specifiers and their modifiers**
There are four integer format specifiers: "%d", "%i", "%u", and "%o".
-  "%d" - this is a decimal format specifier used to output a decimal number. The number can be positive or negative. By default, the output is right-justified, but you can add a field width modifier to specify the minimum width of the output field. You can also add a precision modifier to specify the number of digits after the decimal point.
-  "%i" - used for integer numbers
-  "%u" - used for unsigned integer numbers
-  "%o" - used for octal numbers.
  
-  Each format specifier has optional field width and precision modifiers.
-  The field width modifier is "-n" and the precision modifier is ".".


**String format specifiers**
There are three string format specifiers: "%s", "%c", and "%[...]".
-  "%c" - used to output a single character.
-  “%[...]" - used to output a sequence of characters.
-  "%s" - used to output a string of characters.
-  Each string format specifier can have a field width and precision modifier.

  
**The field width**
The field width modifier specifies the minimum number of characters that will be output. It's denoted by a "-n" after the format specifier. Example: "%s-10" means the string will have a minimum width of 10 characters. The output will be padded with spaces if the string is shorter than 10 characters.
The field width modifier can also be used with the integer format specifiers to right-justify the output.


**The precision modifier**
This is denoted by a "." after the format specifier. For the **string format specifiers**, the precision modifier specifies the maximum number of characters to output. Example: "%s.10" means the string will be output with a maximum of 10 characters. Any characters beyond the tenth character will be truncated. For the **integer format specifiers**; the precision modifier specifies the number of digits after the decimal point.


**The Length Modifiers**
-  "I" - used to specify that the output should be in decimal format. For example, "printf("%Iu", x)" will print the value of "x" in decimal format.
-  "h" - length modifier is used to specify that the output should be in a specific size of unsigned short. For example, "printf("%hu", x)" will print the value of "x" as an unsigned short.
-  "l" - specifies that the output should be a long integer.
-  "j" - specifies that the output should be a short integer.
-  "L" - specifies that the output should be a long long integer.
-  "q" - is for octal output.
-  "b" - for binary output.
-  "t" - is for a boolean value.


**The Optional Modifiers This can be used with the format specifiers.**
-  "-" sign - left-justifies the output.
-  "0" flag - outputs leading zeros for integers.
-  "+" sign - outputs a plus sign in front of positive numbers.
-  "space" flag - outputs a space before positive numbers.
-  "e" or "E" flag - outputs a number in scientific notation.


**The Order of Evaluation for the Format Specifiers and their Modifiers accordingly;**
-  The format specifier is evaluated.
-  The field width and precision modifiers are evaluated.
-  The optional "+", "-" and "space" flags are evaluated.
-  The "e" or "E" flag is evaluated.


**The conversion specifiers**
-  The "%" character can be followed by a conversion specifier, which tells the printf function what type of data to expect. There are several different conversion specifiers;
-  "%s" - this is a string format specifier, which prints the contents of a string. The contents of the string can be literals, escape sequences or references to other variables.
-  "%c" - is used for characters
-  "%d" - is used for signed integers
-  "%u" - is used for unsigned integers
-  "%x" or "%X" - is used hexadecimal numbers. They both output hexadecimal numbers. The only difference is that "%x" uses lowercase letters, while "%X" uses uppercase letters.
-  "%o" - is used for octal numbers
-  "%f" - is used for floating-point numbers
-  "%g" - is used for general-purpose numbers. It prints a floating-point number in either scientific notation or decimal format.
-  "%p" - is used for addresses. It prints a pointer
-  "R" - converts to a wide character string
-  "r" - converts to a multibyte character string.
-  "S" - converts values to a string of characters, and it specifies that the string should be null-terminated.
-  "b" - converts values to an array of characters.
-  "n" - it doesn't actually print anything - instead, it returns the number of characters printed so far.


**Other features of the printf function**
-  "*" character - it indicates a variable argument list. It is useful when you have a variable number of arguments to pass to the printf function.
-  "\" character - it is used to escape special characters like "n", "t", and "b".
-  "-" flag - it left-justifies the output.
-  "l" or "ll" flag - it forces long integer types to be used.

  
  **Pointers**
   Pointers are a special type of variable that stores the address of another variable, rather than the value of that variable. This allows us to access the value of the other variable using the pointer.

**Pointer Type | Description**
-  "x" - General pointer, can point to any data type
-  "R" - Read-only pointer, can only read data
-  "S" - Static pointer, bound to a specific memory location
-  "b" - Bit-field pointer, points to a specific bit within a data structure
-  "p" - Void pointer, can point to any data type.
-  "i" - an incomplete pointer, it is a pointer that points to an incomplete type.
-  "h" - a far pointer, which is a pointer that points to a memory location that's outside the current address space.
-  "#" - a wildcard pointer, which is a pointer that can point to any location in memory.
-  "\x" - an explicit pointer, which is a pointer that's explicitly cast to a specific type.


**Flag characters**
-  Comma (,) - used to separate multiple format specifiers. For example, "printf("%f, %d")" will print a floating-point number and then an integer.
-  Period (.) - used to indicate that the output should be right-justified. For example, "printf("%.2f", x)" will print the value of "x" right-justified with 2 decimal places.
-  Pound sign (#) - used to specify that the output should be hexadecimal.
-  The space character - is also a flag character, and it's used to specify that there should be a space between each item of output. For example, "printf("%f %d", x, y)" will print the value of "x" followed by a space, and then the value of "y".
-  Single quote (') - is yet another flag character. It's used to specify that the output should be a character rather than a number. For example, "printf("%c", x)" will print the character represented by the value of "x". And if "x" is the character 'A', then the output will be 'A'.
-  "..." ellipsis brackets - it means that the function will print additional values that are not specified in the format string. The "printf" function will look at the type of the variable that's being printed and print it in the appropriate format. It should only be used when printing multiple values.

**AUTHOR(S):**
**1**. **Immaculata Gregory Etukenyin**

**2**. **Chioma Victor**
