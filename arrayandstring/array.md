# Arrays in C
## define and declare array
When defining an array, its **size** must be given.

But when just declaring an array without defining it, the size is omitted;

```c
int a[ ];             \\ just declare, not defined

int a[10];  \\defined

int a[ ]={0,1,2,3,4}; \\ undefined size of array
int a[5]={0,1,2,3,4}; \\ full array
int a[2]={0,1,2,3,4}; \\ compile error
int a[8]={0,1,2,3,4};  \\ still have empty slots in array
```

## Initialized
Examples are above