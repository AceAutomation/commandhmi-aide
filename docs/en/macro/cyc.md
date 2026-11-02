# Loop structure program

The loop structure is an important structure of program. When the given condition is satisfied, one program segment is executed repeatedly until the condition is unsatisfied. The given condition is called loop condition, and the program segment executed repeatedly is called loop body. C language provides many loop statements, which may compose different loop structures.

**1.  While statement**

The general form of while statement: While (expression) statement;

wherein, the expression is loop condition, and the statement is loop body.

Semanteme of while statement: compute the expression value. When the value is true (not 0), the loop body statement is executed.

There are some points to be noted in while statement:

1\.  The expression of while statement is usually the relational expression or logical expression. As long as the expression value is true (not 0), it can continue loop.

2\.  If the loop body contains one or more statements, it must be bracketed with {} to form the compound statement.

3\.  Note the loop conditions to avoid endless loop.

**2.  Do-while statement**

General form of do-while statement:

```c
do statement;
while (expression);
```

Wherein, the statement is loop body, and the expression is the loop condition. Semanteme of do-while statement:

First execute the loop body statement for one time, then judge the expression value. If the value is true (not 0), the loop is continuous; otherwise the loop ends.

The difference between do-while statement and while statement is that do-while executes first and judges late. Therefore, do-while will execute the loop body for one time at least. But while statement judges first and executes late. If the condition is unsatisfied, the loop body statement is not executed for one time.

while statement and do-while statement is usually mutual re-write.

In this example, the loop condition is rewritten to be –n. Otherwise, one more loop will be executed. There are some points to be noted in do-while statement:

1\.  In the if statement and while statement, no semicolon is added behind the expression; while the expression of do-while statement must be ended with semicolon.

2\.  do-while statement may be composed to the nested loop and nested with while statement mutually.

3\.  The loop body between do and while is made up of several statements, and bracketed with {} to form a compound statement.

4\.  When converting do-while and while statement mutually, pay attention to modify the loop control conditions.
