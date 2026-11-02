# Branch structure program

**Relational operator and expression**

In the program, it usually compares the size of two data so as to confirm the next process. The operator for comparing data size is called the relational operator. There are such relational operators in C language as following:

&lt;   less than

&lt;= less than or equal to

&gt; greater than

&gt;= greater than or equal to

== equal to

!= unequal to

The relational operator is binary operator, which is left associative. Its priority is lower than that of arithmetic operator and higher than that of assignment operator. In the six relational operators, &lt;,&lt;=,&gt;,&gt;= has the same priority, which is higher than ==   and !=. While ==    and != has the same priority.

**Relational expression**

The    general    form    of    relational    expression    is    Expression    Relational    operator    Expression.    For    example, a+b&gt;c-d,x&gt;3/2,'a'+1&lt;c,-i-5\*j==k+1 are legal relational expression. As the expression is relational expression concurrently, the nestification may occur such as a&gt;(b&gt;c),a!=(c==d) etc. The value of relational expression is "true" and "false", which is expressed with "1" and "0".

**1.  Logical operator and expression**

In C language, the logical operators include AND operator &&, OR operator \|\| and NOT operator !. AND operator && and OR operator \|\| are binary operators with left associativity. NOT operator ! is unary operator with right associativity. The priority relation between logical operator and other operators can be expressed as following:

The following can be derived depending on the priority of operator:

a&gt;b && c&gt;d is equivalent to (a&gt;b) &&   (c&gt;d)

!b==c\|\|d&lt;a is equivalent to ((!b)==c)\|\|(d&lt;a)

a+b&gt;c && x+y&lt;b is equivalent to ((a+b)&gt;c) && ((x+y)&lt;b) Evaluation of logical operation

The evaluation of logical operation may be true or false expressed with 1 and 0 individually. Its evaluation rules are as following:

1\.  When the two values of AND operation && are true, the results are true; otherwise they are false. For example, 5&gt;0

&& 4&gt;2. As 5&gt;0 is true and 4&gt;2 is true, the corresponding result is true.

2\.  When one of two values involved in OR operation \|\| is true, the result is true. When two values are false, the result is false. Take an example of 5&gt;0\|\|5&gt;8. As 5&gt;0 is true, the corresponding result is true.

3\.  When the NOT operation! involved in operation is true, the result is false; when the involved operation is false, the result is true.

For example, the result of !(5&gt;0) is false.

In the logical operation value of C programming, it represents “true” with “1” and represents “false” with “0”. Vice versa, when judging a value is true or false, 0 represents false and the non-zero data represents true. For example, as 5 and 3 are non zero, the value of 5&&3 is “true” (i.e. 1).

Another example: the value of 5\|\|0 is “true” (i.e. 1).

The general form of logical expression is Expression – Logical operator – Expression. Wherein, the expression can be logical expression as well, which forms nestification? Take the (a&&b) &&c as an instance. The above expression can be written to a&&b&&c according to the left associativity of logical operator. The value of logical expression is the final value of various logical operation, which represents “true” and “false” with “1” and “0” respectively.

**2.  if statement**

The branch structure can be constituted with if statement. It makes judgment according to the given conditions so as to confirm what branch program period is to be executed. If statement of C language has three basic forms.

1\.  The first form is: basic form. if (expression) statement

It’s semanteme: if the expression value is true, the following statement will be executed, otherwise not.

2\.  The second form is if-else. if(expression)

statement 1; else statement 2;

Semanteme: if the expression value is true, it will execute statement 1; otherwise statement 2.

Input two integers, and output the bigger one. Judge a and b size with if-else statement. If a is bigger, it outputs a;

otherwise b.

**3.  The third form is if-else-if form.**

In the first two forms, if statement is normally used for two branches. When there are several branches for selection, if-else-if statement is adopted. Its basic form is:

if(expression 1)

statement 1;

else if(expression 2)

statement   2;

else if(expression 3)

statement   3;

…

else if(expression m)

statement m; else statement n;

Semanteme: judge the expression value in sequence. When a value is true, it executes the corresponding statement. Then it executes program out of if statement. If all expressions are false, it will execute statement n. Then continue to execute the subsequent program.

**There are some points to be noted in if statement:**

(1)   In the three forms of if statement, the one behind if is expression. This expression is usually the logical expression or relational expression. But it may be other expressions such as assignment expression even a variable. For example, if(a=5) statement and if(b) statement are allowable. As long as the expression value is not 0, it is true. If the expression value in if(a=5)…; expression is always not 0, the subsequent statement will be executed. This kind of situation may not take place in the program, but the syntax is legal.

Another example, program segment: if(a=b)

```c
printf("%d",a); else printf("a=0");
```

Semanteme of the statement: assign b to a. if it is not 0, this value is output; otherwise it outputs “a=0” character string. This kind of application usually occurs in the program.

(2)   In if statement, the conditional judgment expression must be included in bracket, and ended with semicolon.

(3)   In the three forms of if statement, all statements should be single statement. If a group (several) statements are required execution with conditions, this group of statements must be bracketed with {} to form a compound statement. Pay attention that no semicolon is allowed behind }.

For example:

```c
if(a>b){ a++; b++;
}
else{ a=0;
b=10;
}
```

**4.  Conditional operator and conditional expression**

If the single assignment statement is executed only in the conditional statement, it is usually realized by conditional expression, which not only simplifies the process but also improves the operation efficiency.

Conditional operator ? and : is a ternary operator, which means three values are involved in operation. The general form of conditional expression composed by conditional operators is:

Expression 1 ? Expression 2: Expression 3

Its evaluation rule: if the expression 1 is true, its value of expression 2 will be the value of conditional expression; otherwise, the value of expression 2 will be the value of whole conditional expression. Conditional expression is normally applied in assignment statement. For example:

```c
if(a>b) max=a;
else max=b;
```

max=(a&gt;b)?a:b; is expressed with conditional expression. Its semanteme is: if a&gt;b is true, assign a to max; otherwise assign b to max.

In the application of conditional expression, there are some points to be noted as following:

1\.  The operation priority of conditional operator is lower than that of relational operator and arithmetic operator but higher than assignment operator. Therefore, max=(a&gt;b)?a:b can be removed the bracket to be max=a&gt;b?a:b.

2\.  Conditional operator ? and : is a pair of operator, which can not be separated in application.

3\.  The associative direction of conditional operator is from right to left.
