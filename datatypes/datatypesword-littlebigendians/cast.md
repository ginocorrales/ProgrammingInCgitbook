# Cast

A cast converts the value held in variable x to type T.

`(T) x`

With pointers, casts do not affect the content of the variable

```c
char *c;
int *i;
i = (int *) c;
```

s