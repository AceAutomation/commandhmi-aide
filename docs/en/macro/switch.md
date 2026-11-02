# switch statement

C language provides another switch statement for selection of multiple branches. Its general form is:

switch(expression){

```c
case constant expression 1: statement 1;
case constant expression 2: statement 2;
```

…

```c
case constant expression n: statement n;
default: statement n+1;
}
```

Semanteme: calculate the expression value, and compare with the subsequent constant expression value one by one. When the expression value is equal to a constant expression value, the subsequent statement is executed. Then judgment is not made. Continue the statement behind all case. If the expression value is different from the constant expression behind case, it will execute the statement behind default.

There are several points to be noted in switch statement:

1\.  All constant expression values behind case must be different, otherwise there will be mistake.

2\.  Several statements are allowed behind case, and they can not be bracketed with {}.

3\.  The sequence of case and default clauses may be changed and will not affect the program execution.

4\.  Default clause may be omitted
