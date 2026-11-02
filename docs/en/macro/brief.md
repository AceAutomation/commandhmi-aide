# Section summary

**1.  C data type**

Basic type, construction type, pointer type and void type

**2.  Classification and characteristics of basic type**

|                   |        |                                         |
|-------------------|--------|-----------------------------------------|
| Type Specifier    | Byte   | Number Range                            |
| char              | 1      | C character set                         |
| int               | 4      | -214783648～214783647                   |
| short int         | 4      | -214783648～214783647                   |
| long int          | 8      | -922337203685477808～922337203685477807 |
| unsigned          | 4      | 0～4294967295                           |
| unsigned long     | 8      | 0～1844744073709551615                  |
| float             | 4      | 3/4E-38～3/4E+38                        |
| double            | 8      | 1/7E-308～1/7E+308                      |

**3.  Constant suffix**

L or l for long int

U or u for unsigned

F or f for float

**4.  Constant type**

Int, long int, unsigned, float, char, char string, symbol constant, and escape character

**5.  Data type conversion**

Auto conversion

The system realizes auto conversion for the hybrid operation of different types of data, which converts from small byte data to big byte data. For the mutual assignment of different data, the system also converts automatically, which converts the right data type into left one.

Forced conversion

It is converted by forced conversion operator.

**6.  Priority and associativity of operator**

Generally speaking, the unary operator has higher priority and the assignment operator has lower priority. The arithmetic operator has higher priority, and the relational and logical has lower priority. Most operators have left associativity, unary operator, ternary operator and assignment.

**7.  Expression**

Expression is the formula composed with connection constant, variable and function of operator. Each expression has one value and type. The evaluation of expression is made according to the sequence specified by priority and associativity of operator.

**8.  Array**

1\.  Array is the commonest data structure in program design. The array contains numerical array (int array, float array), character array and pointer array, structure array to be described later.

2\.  Array may be one-dimensional, two-dimensional or multi-dimensional.

3\.  The type declaration of array consists of type specifier, array name and array length (elements quantity of array). The array element is also called subscript variable. The array type refers to the value type of subscript variable.

4\.  Make array assignment with three methods: initialization assignment, dynamic assignment by inputting function and assignment statement. The numerical array can not be overall assigned, input or output with assignment statement but assigned for array element one by one with do statement.
