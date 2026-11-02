# Data type of C language

**1.  Integer**

Integer includes integer constant and integer variable. The integral constant is the integer constant. In C language, there are three kinds of integer constant: octal, hexadecimal and decimal.

**2.  Integer constant**

1\.  Octal integer constant

The octal integer constant must begin with 0. That is to say, 0 is the prefix of octal integer constant. Its value is 0-7.Octal constant is usually unsigned. The followings are the legal octal:

015 (decimal:13) 0101 (decimal:65) 0177777 (decimal:65535)

The followings are the illegal octal: 256 (without prefix 0)    03A2 (contained non-octal codes)             -0127(with negative sign)

2\.  Hexadecimal integer constant

The hexadecimal integer constant is prefixed with 0X or ox. Its value is 0-9, A-F or a-f.

The followings are the legal hexadecimal:

0X2A (decimal:42) 0XA0 (decimal:160)    0XFFFF (decimal: 65535) The followings are the illegal hexadecimal:

5A (without prefix 0X)                0X3H (contained non-hexadecimal codes)

3\.  Decimal integer constant

The octal integer constant has no prefix. Its value is 0-9. The followings are the legal decimal:

237   -568   65535    1627

The followings are the illegal decimal:

023 (prefix 0 is forbidden)          23D (contained non-decimal codes)

In the program, these notations are distinguished by prefix. Therefore, do not mistake the prefix in writing to avoid incorrect result.

4\.  When the suffix of integer constant is on the 16-bit computer, its basic integer is 16-bit. Therefore, the indicated figure value is limited. The decimal unsigned constant is within 0 ～ 65535, and the signed range is -32768 ～+32767.The unsigned octal number is ranged within 0 ～ 0177777. The unsigned hexadecimal number is within 0X0～0XFFFF or 0x0～0xFFFF.If the figure is beyond the above range, it must indicate with long integer. The long integer is suffixed with "L" or "l". For example:

Decimal long integer constant 158L (decimal: 158)   358000L (decimal: -358000)

Octal long integer constant    012L (decimal: 10)   077L (decimal: 63)    0200000L (decimal: 65536)

Hexadecimal long integer constant   0X15L (decimal: 21)    0XA5L (decimal: 165)   0X10000L (decimal: 65536). There is no difference between long int 158L and basic int constant 158. As 158L is the long integer, C compiling

system will assign 4-bit space for storage. As 158 is the long integer, C compiling system will assign 2-bit space for storage. Therefore, pay attention to operation and output format to avoid mistakes. The unsigned number can be indicated with suffix. The unsigned number of integer constant is suffixed with "U" or "u". For example:     358u,

0x38Au, 235Lu are the unsigned number. Use prefix and suffix together to indicate different figures. For example,

0XA5Lu indicates the hexadecimal unsigned long int A5 and the corresponding decimal is 165.

**3.  Integer variable**

The integer variable can be classified as following:

1\.  Int

Its type specifier is int, which occupies 2 bytes in the memory. Its value is always basic integer.

2\.  Short int

Its type specifier is short int or short'C110F1. The occupied bytes and value range is same to basic int.

3\.  Long int

Its type specifier is long int or long, which occupies 4 bytes in the memory. Its value is always long integer.

4\.  Unsigned int

Its type specifier is unsigned.

The unsigned int can be integrated with the above three types:

(1)   The type specifier of unsigned int is unsigned int or unsigned. (2)   The type specifier of unsigned short int is unsigned short.

(3)   The type specifier of unsigned long int is unsigned long.

All unsigned int occupies the same memory bytes with the signed int. As the sign bit is omitted, it can not indicate the negative number. The following table lists the assigned memory bytes and number range of various integers in ARM.

|                |                                        |                |
|----------------|----------------------------------------|----------------|
| Type Specifier | Number Range                           | Assigned Bytes |
| Int            | -2147483648~2147483647                 | ■■■■           |
| Short int      | -2147483648~2147483647                 | ■■■■           |
| Signed int     | -2147483648~2147483647                 | ■■■■           |
| Unsigned int   | 0~4294967295                           | ■■■■           |
| Long int       | -922337203685477808~922337203685477807 | ■■■■■■■■       |
| Unsigned long  | 0~18446744073709551615                 | ■■■■■■■■       |

**4.  Integer variable declaration**

The general form of variable declaration: type specifier, variable name identifier, …. Take examples as following:

```c
int a,b,c; (a,b,c is integer variable)
long x,y; (x,y is long integer variable)
```

unsigned p,q;    (p,q   is unsigned integer variable)

Announcements in writing variables should be paid attention as following:

1\.  Several same type of variables can be allowed to indicate after the same type specifier. Space the variable names with comma. There must be a space at least between the type specifier and variable name.

2\.  The last variable name must be ended with ";".

3\.  The variable declaration must be in front of variable usage. It is always at the head of function body.

\[Practice\]    //1int a,b;

short int c; short d=100; a=d-20; b=a+d;

```c
c=a+b+d;
d=d-a+c-b.
```

**5.  Float constant**

Real constant is also called float constant. Real constant is also called float constant. In the C language, the float is indicated with decimal only. It has two forms as following: Decimal form and exponential form

1\.  Decimal form

It is composed with figure 0-9 and decimal point. For example: 0.0,.25,5.789,0.13,5.0,300.,-267.8230 are the legal float number.

2\.  Exponential form

It is composed of decimal digit, exponent symbol "e" or "E" and exponent (be integer only, symbol is possible). The basic form is an E n (a is decimal, n is decimal integer) and the value is a\*10,n. For example, 2.1E5 (equal to 2.1\*10,5), 3.7E-2    (equal to 3.7\*10,)-2\*) 0.5E7 (equal to 0.5\*10,7), -2.8E-2 (equal to -2.8\*10,)-2\*). The following are the illegal float number: 345 (without decimal point)      E7 (without figure before exponent symbol) -5 (without exponent symbol) 53.-E3   (negative sign is incorrect) 2.7E (without exponent)

The standard floating number in C language has suffix. The figure with suffix "f" or "F" is the floating number. For example, 356f and 356 is equivalent.

**6.  Float variable**

The float variable includes single and double. Their type specifiers are float and double. In the Turbo C, the single occupies four bytes (32-bit) memory, and it is ranged between 3.4E-38～3.4E+38, which provides seven effective figures only. The double occupies 8 bytes (64-bit) memory, and the value is ranged between 1.7E-308 ～ 1.7E+308, which

provides sixteen effective figures.

The form and written rules for float variable declaration is same with that of integer. For example:  float x,y;    (x,y is single float)

double a,b,c;   (a,b,c is double float)

The float constant is not classified into single and double. All float constants are processed as double. a   ■■■■

b   ■■■■■■■■

a&lt;---33333.33333

b&lt;---33333.33333333333;

\[Practice\]    //float int a=32; float b;

double d; b=12345678; d=b\*100;

```c
d=d+a;
d=d+58.123456;
```

**7.  Character**

Characters include character constant and character variable. Character constant

Character constant is a character within single quote. For example, 'a'. 'b', '=', '+', , '?' are the legal character constants. In the C language, the character constants are always characterized as following:

1.   Character constant must be included in single quote rather than double quotes or other brackets.

2.   Character constant must be single character rather than character string.

3.   Character may be any character in the character set. However, the figure cannot be involved in numerical operation after been defined as character. For example, '5' and 5 is different. '5' is character constant that are not involved in operation.

**8.  Character variable**

The character variable value is character constant, i.e. single character. Its type specifier is char. The form and written rules of character variable declaration is same with that of integer variable.

For example:

char a,b;

As each character variable is assigned to a byte memory, one character is saved only. The character value is kept in the memory unit with ASCII code. For example, the decimal ASCII code for x is 120, and the decimal ASCII code for y is

121\. Give 'x' and 'y' to character variable a and b: a='x', b='y'. Actually, it is to store 120 and 121 BC in a and b unit:

a 0   1    1   1    1   0    0   0 b 0   1    1   1    1   0    0   1

Therefore, they can be regarded as integer. C language allows to give character value to integer variable and give integer to character variable as well. It can output character variable as integer and output integer as character. The integer is

2-byte, and character is single byte. When the integer is processed as character, the low eight bytes are involved only. \[Practice\]    //charint a=49;

char b; char d; b=a+10; d=a+b;

\[Practice\]    //char c1,c2;

```c
c1='a';c2='b';
c1=c1-32;c2=c2-32;
```

**9.  Character string constant**

Character string constant is a character string included in double quotes. For example: "CHINA". "C program", "\$12.5", they  are  legal  character  string  constants.  The  character  string  constant  is  different  from  character  constant.  Their differences are described as following:

1\.  Character constant is included in single quotes while character string constant is included in double quotes.

2\.  Character constant is single character only while character string constant contains one or several characters.

3\.  A character can be given to a character variable, but a character string constant can not. In the C language, there is no corresponding character string variable.

4\.  The character constant occupies one byte in the memory. The bytes of character string constant are equal to the bytes of character string plus 1. Save character "\0" (ASCII code:0) in the increased byte. This is the ending symbol of character string. For example, the byte of "C program" in memory is C program\0. Although the character constant 'a' and character string constant ''a'' has one character both, their memory occupation is different.

'a' occupies one byte in the memory, which is indicated as a

''a'' occupies two bytes in the memory, which is indicated as a\0 symbol constant.

**10. Symbol constant**

In the C language, a constant can be expressed with an identifier, which is called symbol constant. It must be defined before usage. Its general form is:

\#define symbol constant

Wherein, \#define is a preprocessor directive, which is called macro definition directive. It is used to define the identifier to the constant value. Upon definition, all of this identifier in the future program will be replaced by the constant value. Usually, the identifier of symbol constant is expressed with capital letter and the variable identifier is expressed with lowercase letter for distraction.

```c
#define PI 3.14159 void main(){
float s,r; r=5; s=PI*r*r;
printf("s=%f\n",s);
}
```

It is defined by macro definition directive. P1 is defined to be 3.14159, and s,r is defined to be float.    5-&gt;r     PI\*r\*r-&gt;s

Display program result float s,r. wherein, r=5, s=PI\*r\*r. This program is defined by macro definition directive before main function. P1 is 3.14159, which substitutes for P1 in the program. s=PI\*r\*r is equivalent to s=3.14159\*r\*r. Pay attention: symbol constant is not variable. Its value can not be changed in the overall action scope. That is to say, assignment statement is forbidden to re-assign in the program.
