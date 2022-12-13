# Libft - Library of Functions /42 Lisboa/

This is my `first project` as a `42 Lisboa` student, where I had to `create a library` containing multiple `libc re-coded functions` and also `create new ones that are not included in the standard C library`.

So, the project was divided in `3 parts`:

- In the `first part`, I re-coded some functions of the standard C library, following the steps in their man, making them have the same behaviors and prototypes as the original ones. All of their names had to start by the prefix "ft_XXX.c", according to the pdf project's instructions;

- Meanwhile, in the `second part`, I coded some additional functions that are not present in the standard C library, or are included in a different form;

- And in the `last part`, I worked with the concept of linked list functions, as a bonus for receiving extra points in my project's evaluation.

To do these steps, I worked with `3 different types of files`, them being:

- `.c` -> Is the file format that all of the functions written must have;

- [`.h`](libft.h) -> It represents the header for the functions, which is useful because I just needed to include it once, and all of the .c files would read from it - by doing this I don't need to put the header of a function (#include <stdio.h>, for example) in every single file. Also, if one function references another function of the library, the header file saves time once I don't need to write the function again;

- [`Makefile`](Makefile) -> Is the file that compiled all of the functions and header of my project as a whole - that way I didn't need to create an "int main" and compile the functions with the "gcc" flags. I only needed to type "make" once I had it created.

`Functions`:

A) Functions from the library `<ctype.h>`:

- [`ft_isalpha`](ft_isalpha.c) - used to check if the param is an alphabetic character ( a-z || A-Z ).
- [`ft_isdigit`](ft_isdigit.c) - used to check if the param is a digit ( 0-9 ).
- [`ft_isalnum`](ft_isalnum.c) - used to check if the param is an alphanumeric character ( a-z || A-Z || 0-9 ).
- [`ft_isprint`](ft_isprint.c) - used to check if the param is a printable character.
- [`ft_isascii`](ft_isascii.c) - used to check if the param is part of the ASCII character set.
- [`ft_tolower`](ft_tolower.c) - used to convert char to lowercase characters.
- [`ft_toupper`](ft_toupper.c) - used to convert char to uppercase characters.

B) Functions from the library `<string.h>`:
- [`ft_strlen`](ft_strlen.c)	- used to calculate the length of a string.
- [`ft_strchr`](ft_strchr.c)	- used to locate the first occurence of a character in string, returning a pointer to it.
- [`ft_strrchr`](ft_strrchr.c)	- used to locate the last occurence of a character in string.
- [`ft_strncmp`](ft_strncmp.c)	- used to compare two strings, returning a value according to the difference of the first character they differ.
- [`ft_strnstr`](ft_strnstr.c)	- used to locate a substring in a string.
- [`ft_strdup`](ft_strdup.c)	- creates a duplicate for the string passed as parameter.
- [`ft_strlcpy`](ft_strlcpy.c)	- used to copy a string to an specific size.
- [`ft_strlcat`](ft_strlcat.c)	- used to concatenate a string to an specific size.
- [`ft_bzero`](ft_bzero.c)	- used to write a specific amount of zero bytes to a string.
- [`ft_memset`](ft_memset.c)	- used to fill the memory with a constant byte.
- [`ft_memcpy`](ft_memcpy.c)	- used to copy memory area, returning original value of dst.
- [`ft_memmove`](ft_memmove.c)	- used to copy memory area like memcpy, but more useful if src and dst overlap.
- [`ft_memchr`](ft_memchr.c)	- used to scan memory to find the first occurence of a character in a buffer.
- [`ft_memcmp`](ft_memcmp.c)	- used to compare different memory areas.

C) Functions from the library `<stdlib.h>`:
- [`ft_atoi`](ft_atoi.c)	- used to convert a string to an integer.
- [`ft_calloc`](ft_calloc.c)	- used to allocate memory and set its bytes' values to 0.

D) `Non-standard` functions:
- [`ft_substr`](ft_substr.c)	- used to return a substring from a string.
- [`ft_strjoin`](ft_strjoin.c)	- used to concatenate two strings.
- [`ft_strtrim`](ft_strtrim.c)	- used to trim the beginning and end of string with specific set of chars.
- [`ft_split`](ft_split.c)	-used to split a string using a char as parameter.
- [`ft_itoa`](ft_itoa.c)	- used to convert a number into a string.
- [`ft_strmapi`](ft_strmapi.c)	- used to apply a function to each character of a string.
- [`ft_striteri`](ft_striteri.c)	- used to apply a function to each character of a string like ft_strmapi - but not using malloc.
- [`ft_putchar_fd`](ft_putchar_fd.c)	- used to output a char to a file descriptor.
- [`ft_putstr_fd`](ft_putstr_fd.c)	- used to output a string to a file descriptor.
- [`ft_putendl_fd`](ft_putendl_fd.c)	- used to output a string to a file descriptor, followed by a new line.
- [`ft_putnbr_fd`](ft_putnbr_fd.c)	- used to output a number to a file descriptor.

E) `Linked list` functions:
- [`ft_lstnew`](ft_lstnew.c)	- used to create a new node in a list.
- [`ft_lstadd_front`](ft_lstadd_front.c)	- used to add a new node at the beginning of a list.
- [`ft_lstsize`](ft_lstsize.c)	- used to count the number of nodes inside a list.
- [`ft_lstlast`](ft_lstlast.c)	- used to return the address of the last node of a list.
- [`ft_lstadd_back`](ft_lstadd_back.c)	- used to add a new node at the end of a list.
- [`ft_lstclear`](ft_lstclear.c)	- used to delete a node's content and free its memory from the list.
- [`ft_lstdelone`](ft_lstdelone.c) - used to delete a node's content and free its memory from the list.
- [`ft_lstiter`](ft_lstiter.c)	- used to apply a function to each node of a list.
- [`ft_lstmap`](ft_lstmap.c)	- used to apply a function to each element of a list, creating and returning a new list.
