# Initial value of variable and type conversion

**1.  Initial value assignment for variable**

In the program, it is usually to assign initial value for the variable. There are many methods for initial value assignment in the language program, which are called initialization. In the variable declaration, the general form of initial value assignment is:

Type specifier variable 1 = 1, variable 2 = 2, ……; for example:

```c
int a=b=c=5;
float x=3.2,y=3f,z=0.75;
char ch1='K',ch2='P';
```

Note: no continuous assignment is forbidden in the declaration, for instance a=b=c=5 is illegal.

**2.  Type conversion of variable**

The variable type is convertible. There are two methods for conversion. One is automatic conversion, the other is forced conversion.

Automatic conversion

When the different types of data are involved in hybrid operation, the automatic conversion is completed by compilation system. The auto conversion should conform to the following rules:

1\.  If the data types involved in operation are different, first convert them into one type, then make operation.

2\.  Conversion is made as the data length so as to ensure the high precision. For example, when int and long is in operation, convert int into long, then make operation.

3\.  All float operations are double. Even the expression contains float only, it must be converted to double for operation.

4\.  Char and short must be converted into int for operation.

5\.  In the assignment operation, when the data types on both sides of assignment sign are different, the right data type will be converted to the left type. If the right data is longer than left one, it will loss a part of data. In this case, the precision will be reduces. The lost data will be rounded off.

**3.  Forced type conversion**

The forced type conversion is achieved by type conversion operation. Its general form is (type specifier) (expression). It is used to convert the operation results into the specified type of type specifier by force. Take an example of (float) a. convert a to float (int)(x+y), convert the result of x+y into integer. In forced conversion, there are some points to be noted:

1\.  Type specifier and expression must be included in the bracket (the single variable may not be bracketed). If (int)(x+y)

is written to be (int)x+y, it means to convert x into int and plus y.

2\.  Either forced conversion or auto conversion is just the temporary conversion of data length for convenience of the operation. It will not change the variable type in the data declaration.
