# Libft

## Summary

Libft is a custom implementation of the standard C library functions. It is a foundational project in the 42 curriculum that helps students understand and recreate essential functions from the C standard library. The project involves writing functions for memory management, string manipulation, linked lists, and other utility functions.

### Key Features

- **Memory Management**: Functions to allocate, deallocate, and manipulate memory.
- **String Manipulation**: Functions to handle and manipulate C strings.
- **Linked Lists**: Basic linked list operations.
- **Utility Functions**: Various helper functions to perform common tasks.

### Project Structure

The project is divided into several parts:

1. **Libc Functions**: Reimplementation of standard libc functions.
2. **Additional Functions**: Extra functions that are not part of the standard library but are useful.
3. **Bonus Part**: Implementation of linked list functions.

### Full Functions

#### Memory Management

- `void *ft_memset(void *b, int c, size_t len);` - Fills memory with a constant byte.
- `void ft_bzero(void *s, size_t n);` - Sets memory to zero.
- `void *ft_memcpy(void *dst, const void *src, size_t n);` - Copies memory area.
- `void *ft_memccpy(void *dst, const void *src, int c, size_t n);` - Copies memory until a character is found.
- `void *ft_memmove(void *dst, const void *src, size_t len);` - Moves memory area.
- `void *ft_memchr(const void *s, int c, size_t n);` - Scans memory for a character.
- `int ft_memcmp(const void *s1, const void *s2, size_t n);` - Compares memory areas.

#### String Manipulation

- `size_t ft_strlen(const char *s);` - Computes the length of a string.
- `char *ft_strdup(const char *s1);` - Duplicates a string.
- `char *ft_strcpy(char *dst, const char *src);` - Copies a string.
- `char *ft_strncpy(char *dst, const char *src, size_t len);` - Copies a string with length limit.
- `char *ft_strcat(char *s1, const char *s2);` - Concatenates two strings.
- `char *ft_strncat(char *s1, const char *s2, size_t n);` - Concatenates two strings with length limit.
- `size_t ft_strlcat(char *dst, const char *src, size_t dstsize);` - Concatenates strings with size limit.
- `char *ft_strchr(const char *s, int c);` - Locates a character in a string.
- `char *ft_strrchr(const char *s, int c);` - Locates a character in a string from the end.
- `char *ft_strstr(const char *haystack, const char *needle);` - Locates a substring.
- `char *ft_strnstr(const char *haystack, const char *needle, size_t len);` - Locates a substring with length limit.
- `int ft_strcmp(const char *s1, const char *s2);` - Compares two strings.
- `int ft_strncmp(const char *s1, const char *s2, size_t n);` - Compares two strings with length limit.

#### Linked Lists

- `t_list *ft_lstnew(void const *content, size_t content_size);` - Creates a new list element.
- `void ft_lstdelone(t_list **alst, void (*del)(void *, size_t));` - Deletes a list element.
- `void ft_lstdel(t_list **alst, void (*del)(void *, size_t));` - Deletes a list.
- `void ft_lstadd(t_list **alst, t_list *new);` - Adds an element at the beginning of a list.
- `void ft_lstiter(t_list *lst, void (*f)(t_list *elem));` - Iterates over a list.
- `t_list *ft_lstmap(t_list *lst, t_list *(*f)(t_list *elem));` - Applies a function to each element of a list.

#### Utility Functions

- `int ft_atoi(const char *str);` - Converts a string to an integer.
- `int ft_isalpha(int c);` - Checks for an alphabetic character.
- `int ft_isdigit(int c);` - Checks for a digit (0 through 9).
- `int ft_isalnum(int c);` - Checks for an alphanumeric character.
- `int ft_isascii(int c);` - Checks for an ASCII character.
- `int ft_isprint(int c);` - Checks for a printable character.
- `int ft_toupper(int c);` - Converts a character to uppercase.
- `int ft_tolower(int c);` - Converts a character to lowercase.

### Usage

To use the library, compile it and link it with your C programs:

```sh
make
gcc -L. -lft your_program.c
```

Include the header file in your source code:

```c
#include "libft.h"
```

### Compilation

Use the provided Makefile to compile the library:

- `make`: Compiles the library.
- `make clean`: Removes object files.
- `make fclean`: Removes object files and the library.
- `make re`: Recompiles the library from scratch.

### Testing

You can write your own tests or use available testing frameworks to ensure the correctness of your functions.

### Conclusion

Libft is an excellent way to deepen your understanding of C programming and the inner workings of the standard library. Completing this project will provide a strong foundation for more advanced programming tasks.