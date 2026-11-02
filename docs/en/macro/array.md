# One-dimensional array

In the program design, the array organizes several variables with same category in ordered form for convenience. The set containing data elements with the same category in order is called array. In C language, the array belongs to construction data. One array can be split into several array elements. These array elements are either basic data or construction data. Therefore, the array can be classified into numerical array, character array, pointer array, structure array according to the category of array element.

This section will introduce the numerical array and character array, others will be described in the successive sections. If the array type declaration uses array in C language, it must be made type declaration first. The general form of array declaration is: type specifier array name    \[constant expression\]. Wherein, type specifier refers to any basic data or construction data. Array name refers to the array identifier defined by users. The constant expression in square bracket indicates the quantity of data elements, which is also called array length.

For example:

int a\[10\]; int array a contains 10 elements.

float b\[10\],c\[20\]; float array b contains 10 elements; float array c contains 20 elements. char ch\[20\]; character array ch contains 20 elements.

For the array type declaration, there are several points as following:

1\.  The array type actually refers to the value type of array element. For the same array, the data type of all elements is the same.

2\.  The writing rules for array name should conform to that of identifier.

3\.  The array name should not be same with other variable name. For example:   void main ()

```c
{
int a;
float a[10];
```

……

} is incorrect

4\.  The constant expression in the square bracket refers to the element quantity. For example, a \[5\] indicates that array a contains 5 elements. However, its subscript is started from 0. Therefore, the five elements are a\[0\],a\[1\],a\[2\],a\[3\],a\[4\].

5\.  The square bracket can not include the element quantity of variables but symbol constant or constant expression is available. For instance:

\#define FD    5

```c
void main ()
{
int a[3+2],b[7+FD];
```

……

```c
} is legal. However, the following expression form is incorrect. void main()
{
int n=5;
int a[n];
```

……

}

6\.  It is allowed that the same type declaration can describe several arrays and several variables.

For example: int a,b,c,d,k1\[10\],k2\[20\];

**1.  Representation of array element**

Array elements are the basic unit of array. It is also a variable, which is identified with array name and a subscript. The subscript indicates the sequence number of element in the array. The general form of array element is: array name \[subscript\]. Wherein, subscript is integer constant or integer expression only. If it has decimal, this value will be integer automatically by C programming. For example, a\[5\],a\[i+j\],a\[i++\] are the legal array elements. Array element is usually called subscript variable. The subscript variable could not be used unless array is defined. In C language, the subscript variable is used one by one rather than the whole array.

The general form of initialization assignment is: static type specifier array name \[constant expression\]=\[value……\]. Wherein, static refers to the static storage type. It is specified that only static storage array and external storage array can be initialized assignment (the relevant static storage and external storage concepts will be introduced in Chapter 5) in C language. The data in {    } are the initial value of each element, and the elements are spaced with comma such as static int a\[10\]={    0,1,2,3,4,5,6,7,8,9   }, which is equivalent to a\[0\]=0;a\[1\]=1...a\[9\]=9;

**2.  There are several provisions for initial assignment of array in C language:**

1\.  It is allowed to assign initial value for partial elements. When the elements in {    } is less than element quantity, the initial value is assigned for the front only. For example: static int a\[10\]={0,1,2,3,4}, it indicates that the initial value

will be assigned for the first 5 elements a\[0\]～a\[4\], and the last 5 elements will be assigned 0 automatically.

2\.  Assign initial value for element one by one, and the overall assignment for array is unavailable. For example, if assigning 1 for 10 elements, it can write to be static int a\[10\]={1,1,1,1,1,1,1,1,1,1} rather than static int a\[10\]=1.

3\.  If the initial value assignment is unavailable for all arrays with initialization, all elements will be 0.

4\.  If assigning all elements, the array element quantity may not be given in the array declaration. For example: static int a\[5\]={1,2,3,4,5} can be written as     static int a\[\]={1,2,3,4,5}. The dynamic assignment can be made during program execution. In this case, it can use do statement and scanf function to assign the array elements one by one.

**3.  Character array**

The array for storing characters is called character array. The form of type declaration for character array is same to that of numerical array as previous introduction. For example: char c\[10\]. As the character and integer is similar, it can be defined as int c\[10\], but each array element occupies 2 bytes in memory. The character array may be two-dimensional array.  For  instance,  char  c\[5\]\[10\]  is  a  two-dimensional  character  array.  The  character  array  is  allowed  to  made initialization assignment in type declaration. Take static char c\[10\]={\`c\`,\`    \`,\`p\`,\`r\`,o\`,g\`,r\`,\`a\`,\`m\`} as an example. After assignment, the element value is c\[0\]c\[1\]c\[2\]c\[3\]c\[4\]c \[5\]c\[6\]c\[7\]c\[8\]c\[9\] for array C. Wherein, c\[9\] is not assigned and assigned to 0 by system automatically. When assigning initial value for all elements, the length declaration can be omitted such as static char c\[\]={\`c\`,\`    \`,\`p\`,\`r\`,\`o\`,\`g\`,\`r\`,\`a\`,\`m\`}, in which the length of C array is set to 9.

C  language  allows  for  initialization  assignment  for  array  in  character  string.  For  example,  static  char  c\[\]={'c',  ' ','p','r','o','g','r','a','m'} can be written to static char c\[\]={"C program"} or static char c\[\]="C program" without {}. The assignment in character string occupies one more byte than assignment one by one. It is used to store the ending sign of character string '\0'. The actual storage of array c in memory is C program\0. Wherein, \`\0' is added by C programming system automatically. As '\0' sign is adopted, the array length is not normally defined in initialization assignment of character string but processed by system automatically. If in the mode of character string, the input and output of character array becomes simple and convenient. Except the initial value assignment with character string, it can input and output the character string of one character array with printf function and scanf function at one time not requiring input/output each character with do statement one by one.
