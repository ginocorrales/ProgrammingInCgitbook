# Data Types

### Base data type

* `int`     -used for integer numbers
* `float`   -used for floating point numbers
* `double`  -used for large floating point numbers
* `char`    -used for characters
* `void`    -used for functions without parameters or return value
* `enum`    -used for enumerations

### The composite types are

* `struct` with fields of other types
* `union` of several types
* `array` of other types
* `pointer` to other types
* `function` with arguments types and a return type

## Qualifiers, Modifiers & Storage

### Type qualifiers

* `short`         decrease storage size
* `long`           increase storage size
* `signed`         request signed representation
* `unsigned`     request unsigned representation

### Type modifiers

* `volatile`       value may change without being written to by the program
* `const`            value not expected to change

## Size

Some data types are not interpreted the same on different platforms, they are **machine-dependent**.

`sizeof( x )` returns the size **in bytes** of the objectx\(either a variable or a type\) on the current architecture.![](/datatypes/lecture/dataSize.png)

## Ref:

Zhiyuan [Li](https://github.com/sean8purdue/ProgrammingInCgitbook/blob/master/datatypes/lecture/dataTypesWordEndians_Li.pdf)

Zhiyuan [Li2](/datatypes/lecture/dataTypesWordEndians_Li.pdf)



