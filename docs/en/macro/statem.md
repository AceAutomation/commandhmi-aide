# Statement of C program

The execution part of C program is constituted by statements, and the program function is also realized by execution statement. C statement is classified into five categories:

1\.  Expression statement

2\.  Control statement

3\.  Compound statement

4\.  Null statement

**1.  Expression statement**

Expression statement consists of expression and semicolon. Its general form is expression;. Execution of expression statement is to compute the expression value. For example, x=y+z; assignment statement y+z; operate statement with addition, but the result is not kept. It has no actual significance i++. Increment 1 statement, i value increases 1.

**2.  Control statement**

Control statement is to control the program process so as to realize various structures of program.

It is composed of special statement delimiter. There are nine control statements in C language, which can be classified into three kinds:

(1)   Conditional judgment statement if statement, switch statement

(2)   Looping execution statement

do while statement, while statement, for statement

(3)   Go to statement

break statement, go to statement, continue statement, return statement

**3.  Null statement**

The statement with semicolon only is called null statement. Null statement executes nothing. In the program, null statement can be the null loop body. Take an example of while (getchar()!='\n'). For this statement, if the character input from keyboard is not Enter, it requires re-input. Here, the loop body is null statement.

**4.  Assignment statement**

Assignment statement consists of assignment expression and semicolon. Its general form is variable = expression. Its functions and features are same to that of assignment expression. It is one of the most popular statements in the program. There are some points to be noted in the usage of assignment statement:

1\.  As the expression on the right of assignment sign "=" can be an assignment expression, the following form Variable=(variable=expression); is established, then the nestification is formed. Its expanded expression is Variable=Variable=…=Expression;

For example:

```c
a=b=c=d=e=5; according to the right associativity of assignment operator, it is equivalent to: e=5 actually;
d=e; c=d; b=c; a=b;
```

2\.  Pay attention to the difference between assigning initial value and statement for variable in the variable declaration.

Assigning initial value to variable is a part of variable declaration. The variable with initial value assignment should be spaced with comma to other similar variable, but the assignment statement must be ended with semicolon.

3\.  In the variable declaration, it is forbidden to assign initial value for several variables successively. For example, the following declaration is incorrect. Int a=b=c=5 must be written to int a=5,b=5,c=5. However, the assignment statement must be assigned continuously.

4\.  Note the difference between assignment expression and assignment statement. Assignment expression is a kind of expression, which can be used in any allowable place. But the assignment statement can not.

The following statement is legal: if((x=y+5)&gt;0) z=x; the function of statement: if expression x=y+5 is greater than 0, then z=0.

The following statement is illegal: if((x=y+5;)&gt;0) z=x; as x=y+5; is a statement, it can not be used in expression.
