# for statement

For statement is a kind of loop statement with stronger function and wider application provided by C language. Its general form is:

For (Expression 1;Expression 2;Expression 3)

statement;

Expression1: it is usually to assign initial value to loop variable, and it is assignment expression. It also allows to assign initial value to loop variable except for statement. In this case, the expression may be omitted.

Expression 2: it is usually the loop condition, and it is relational expression or logical expression. Expression 3: it is usually for modifying the value of loop variable, and it is assignment statement.

These three expressions may be comma expression. That is to say, each expression can be composed with several expressions. Three expressions are options and can be omitted.

The “statement” in general form is loop body statement. Semanteme of for statement is:

1\.  First, calculate the value of expression 1.

2\.  Then, compute the value of expression 2. If the value is true (not 0), loop body is executed once more; otherwise exit the loop.

3\.  Calculate the value of expression 3 and return to execute step 2 again. During the for process, expression 1 is calculated for one time, and expression 2 and 3 may repeat for several times. The loop body may be executed for many times or not executed.

There are several points to be noted in for statement:

1\.  Each expression in for statement can be omitted, but the semicolon must exist. For example:

&lt;1&gt;for(expression; expression) expression is omitted

&lt;2&gt;for(expression; expression;)expression is omitted

&lt;3&gt;for(;expression; expression) all expression is omitted

2\.  When the loop variable has assigned initial value, Expression 1 may be omitted as shown in Example 3.27. If Expression

2 or 3 is omitted, the endless loop may be caused. In this case, the loop should be ended in loop body.

3\.  The loop body may be void statement.

```c
#include" stdio.h" void main(){
int n=0;
printf("input a string:\n"); for(;getchar()!='\n';n++); printf("%d",n);
}
```

In this example, the expression 1 in for statement is omitted, and the expression 3 is not for modifying loop variable but for inputting the characters counting. Thus, the counting that should be completed in loop body has completed in the expression. Therefore, the loop body is void statement. Pay attention, the semicolon behind void statement is essential. If this semicolon is missed, the following printf statement will be executed as loop body. On the other hand, if the loop body is not void statement, it is forbidden to add semicolon behind the bracket of expression. In this case, the loop body will be regarded as void statement and not executed repeatedly. All of these are the common mistakes in programming, which must be attached great importance.
