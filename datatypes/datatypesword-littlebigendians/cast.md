# Cast

A cast converts the value held in variable x to type T.

`(T) x`

With pointers, casts do not affect the content of the variable pointed (merely an indication to the compiler):

```c
char *c;
int *i;
i = (int *) c;
```

s