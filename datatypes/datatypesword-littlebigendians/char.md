# What are characters

characters are just unsigned int in C.

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

##### Second example \(also review type cast\): {#typecast}

```c
#include <stdio.h>

int main() {
    int i;
    int a[ ] = {'a','b','c','d','e'};

    for (i = 0; i < 5; ++i)
        printf("a[%d] = \t %s\n", i, (char *) &a[i]);  // print char
        // note!! 
        printf("a[%d] = \t %c\n", i, (char *) &a[i]);  // %c will have compile error

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

