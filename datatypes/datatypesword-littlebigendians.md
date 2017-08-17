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

## 2's complement (to be continued)
The binary representation of negation of an integer n is obtained by

* First negate n bit-wise
* Add 1 to the least significant bit

Example (8-bit data representation)
> 1’s bit pattern is 0000 0001
> Negation result: 11111110
> Add binary 1, we get: 11111111


## Ref:

Zhiyuan [Li](https://github.com/sean8purdue/ProgrammingInCgitbook/blob/master/datatypes/lecture/dataTypesWordEndians_Li.pdf)

Zhiyuan [Li2](/datatypes/lecture/dataTypesWordEndians_Li.pdf)



