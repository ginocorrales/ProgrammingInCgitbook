# File IO

“In the UNIX operating system, all input and output is done by reading or writing files, because all peripheral devices, even keyboard and screen, are files in the file system. This means that a single homogeneous interface handles all communication between a program and peripheral devices.”

“Since input and output involving keyboard and screen is so common, special arrangements exist to make this convenient.”

“When the command interpreter \(the \`\`shell''\) runs a program, \*\*three files are open, with file descriptors 0, 1, and 2, called the standard input, the standard output, and the standard error\*\*. If a program reads 0 and writes 1 and 2, it can do input and output without worrying about opening files.”

“The user of a program can redirect I/O to and from files with &lt; and &gt;:

`prog < infile > outfile`

“In this case, **the shell** changes the default assignments for the file descriptors 0 and 1 to the named files. Normally file descriptor 2 remains attached to the screen, so error messages can go there.”

“ The file assignments are changed by the shell, not by the program. The program does not know where its input comes from nor where its output goes, so long as it uses file 0 for input and 1 and 2 for output.”

Chapter 8: how in C we can directly interact with Unix OS.

## Stream

Let us go to Appendix B.1 to learn something about &lt;stdio.h&gt;

“A stream is a source or destination of data that may be associated with a disk or other peripheral. The library supports text streams and binary streams, although on some systems, notably UNIX, these are identical.”

“A text stream is a sequence of lines; each line has zero or more characters and is terminated by '\n'. An environment may need to convert a text stream to or from some other representation \(such as mapping '\n' to carriage return and linefeed\).”

“A stream is connected to a file or device by opening it; the connection is broken by closing the stream. Opening a file returns a pointer to an object of type FILE, which records whatever information is necessary to control the stream. We will use `file pointer` and `stream` interchangeably when there is no ambiguity.”

“When a program begins execution, the three streams stdin, stdout, and stderr are already open.”

## Formatted output

```c
int fprintf(FILE *stream, const char *format, ...)
int printf(const char *format, ...)
```

`printf(...)` is equivalent to `fprintf(stdout, ...)`

* char \*format means the \(parameter\) variable “format” is a pointer to a sequence \(of unknown length\) of characters
* `const char *format` means the parameter is a **quoted string**.  
  So, `printf` expects `the first argument` to be a `quoted string` which may include textual characters, escape sequences \(e.g. \n\), and conversion character.

* Each conversion character defines the formatting specification for the corresponding parameter that follows the “format” parameter

## Char I/O

`int getchar(void)`  is equivalent to `fgetc(stdin)`

int putchar\(int c\)

## Ref

[Lecture1](https://github.com/sean8purdue/ProgrammingInCgitbook/blob/master/file-io/lectures/fileIO_ZhiyuanLi.pdf)\_ZhiyuanLi

