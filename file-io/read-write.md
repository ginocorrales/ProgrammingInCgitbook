# Lower Level I/O - read and write

## Basic function

Input and output uses the read and write **system calls**, which are accessed from C programs through two functions called read and write.

For both, the first argument is a file descriptor. The second argument is a character array **in your program** where the data is to go to or to come from. The third argument is the number which is the number of bytes to be transferred.

```c
int n_read = read(int fd, char *buf, int n);
int n_written = write(int fd, char *buf, int n);
```

Each call returns a count of the number of bytes transferred.

**Note**: On reading, the number of bytes returned may be less than the number requested. A return value of `zero bytes implies end of file`, `and -1 indicates an error` of some sort.

For writing, the return value is the number of bytes written; an error has occurred if this isn't equal to the number requested.

## The number read or write

Any number of bytes can be read or written in one call. The most common values are 1, which means one character at a time \(\`\`unbuffered''\), and a number like 1024 or 4096 that corresponds to a physical block size on a peripheral device.

Larger sizes will be more efficient because **fewer system calls** will be made.

## Simple 'cat' Unix command

Using these two syscalls, we can write a simple program to copy its input to its output, the equivalent of the Unix command “cat”.

This program will copy anything to anything, since the input and output can be redirected to any file or device.

```c
#include <sys/types.h> //on Mac for read() write
#include <sys/uio.h>  
#include <unistd.h>

#define BUFSIZ 100

int main() { /* copy input to output */
    char buf[BUFSIZ];
    int n;
    while ((n = read(0, buf, BUFSIZ)) > 0)
        write(1, buf, n); 
    
    return 0;
}
```



