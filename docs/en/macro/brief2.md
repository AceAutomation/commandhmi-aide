# Section summary

1\.  From the execution process, the program is basically classified into three basic structures: sequence structure, branch structure and loop structure.

2\.  The most basic unit in program execution is statement. There are five kinds of statements in C language:

(1)   Expression statement any expression and semicolon forms the expression statement. The general expression statement is assignment statement.

(2)   Function call statement   the function call and semicolon constitutes the function call statement.

(3)   Control statement    it is used for control program process, and composed of special statement delimiter and required expression. It mainly includes conditional judgment execution statement, loop execution statement, go to statement etc.

(4)   Compound statement it is composed by several statements included in {}. Compound statement is regarded as single statement. It can be used in any place allowing statement such as loop body.

(5)   Void statement  it is composed by semicolon only without actual function.

3\.  Relational expression and logical expression are two important expressions, which are mainly used for judgment of conditional execution and loop execution.

4\.  C language provides many forms of conditional statement to form the branch structure. (1)   if statement is mainly for one-way selection.

(2)   if-else statement is mainly for two-way selection.

(3)   if-else-if statement and switch statement are for multiway selection. These forms of conditional statement are normally mutual substituted.

5\.  C language provides three loop statements.

(1)   For statement is mainly used to assign initial value for loop variable, step increment and loop structure of loop times. (2)   The loop times and control condition can be confirmed during loop process, and the confirmed loop may use while

or do-while statement.

(3)   Three loop statements can be nested mutually to form the nested loop. The loops may be in parallel but not crossed. (4)   Branch statement can transfer the process out of loop body, but it can not transfer process from outside to loop body.

(5)   Avoid endless loop in the loop program. That is to say, the loop variable must be ensured to be modified during operation. Change the loop condition to be false gradually, thus finish the loop.

6\.  Statement summary in C language

Name                                General Form

Simple statement                Expression statement; Void statement                           ;

Conditional statement          if(expression)statement;

if(expression)statement 1; else statement 2;

if(expression 1)statement 1;   else if(expression 2) statement 2…else statement n; switch statement                 switch(expression){ case constant statement: statement…default: statement;   } loop statement                           while statement

```c
while(expression)statement;
for statement for(expression 1; expression 2; expression 3) statement; break statement break;
continue statement continue;
return statement return(expression);
```
