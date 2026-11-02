# switch-Anweisung

C bietet außerdem die switch-Anweisung zur Auswahl zwischen mehreren Zweigen. Ihre allgemeine Form ist:

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

Bedeutung: Der Ausdruck wird ausgewertet und nacheinander mit den konstanten Ausdrücken verglichen. Sobald er einem davon gleicht, werden die folgenden Anweisungen ausgeführt, ohne weitere Vergleiche – auch die der folgenden case-Zweige. Gleicht er keinem konstanten Ausdruck, werden die Anweisungen nach default ausgeführt.

Hinweise zur switch-Anweisung:

1\.  Die konstanten Ausdrücke der case-Zweige müssen alle verschieden sein, sonst entsteht ein Fehler.

2\.  Nach einem case können mehrere Anweisungen stehen; sie müssen nicht mit {} geklammert werden.

3\.  Die Reihenfolge der case- und default-Zweige kann geändert werden, ohne die Ausführung zu beeinflussen.

4\.  Der default-Zweig kann entfallen
