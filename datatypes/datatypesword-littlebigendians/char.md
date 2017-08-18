# What are characters

In C, a single character stored in 1 byte, characters are just `unsigned int`(byte size is different).

```c
#include <stdio.h>

int main() {
    int i;
    int a[ ] = {'a','b','c','d','e'};

    for (i = 0; i < 5; ++i)
        printf("a[%d] = \t %d\n", i, a[i]); // print int
}
```

```
a[0] =      97
a[1] =      98
a[2] =      99
a[3] =      100
a[4] =      101
```

Second example \(also **review type cast**\):

```c
#include <stdio.h>

int main() {
    int i;
    int a[ ] = {'a','b','c','d','e'};

    for (i = 0; i < 5; ++i)
        printf("a[%d] = \t %s\n", i, (char *) &a[i]);  // print char
        // note!! 
        printf("a[%d] = \t %c\n", i, (char *) &a[i]);  // %c will have compile error
        // printf(%s, char *); 
        // characters from the string are printed until a '\0' is reached 
        // or until the number of characters indicated by the precision have been printed.
}
```

```
a[0] =      a
a[1] =      b
a[2] =      c
a[3] =      d
a[4] =      e
```

**Notice**: how we recast `&a[i]` to pointer to character, Because this is what the “%s” format must match.

## Null character `\0`

```c
#include <stdio.h> 

int main() {
    printf("Null character has integer value \t %d\n", '\0');
    printf("Null character can be printed as \t %c\n", '\0');
    printf("Null character has hexadecimal value \t %x\n", '\0');
}
```

result:

```
Null character has integer value          0
Null character can be printed as
Null character has hexadecimal value      0
```

## `getchar()` and `putchar()`

Week8-1_bitRotation_Li

