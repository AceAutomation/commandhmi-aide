# switch-instructie

C biedt ook de switch-instructie voor keuzes met meerdere vertakkingen. De algemene vorm is:

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

Betekenis: de waarde van de expressie wordt berekend en één voor één vergeleken met de constante expressies die volgen. Is ze gelijk aan een constante expressie, dan worden de instructies daarna uitgevoerd, zonder verdere vergelijking, inclusief de instructies van alle volgende case-takken. Is ze aan geen enkele constante expressie na case gelijk, dan worden de instructies na default uitgevoerd.

Aandachtspunten bij de switch-instructie:

1\.  Alle constante expressies na case moeten verschillend zijn; anders volgt een fout.

2\.  Na case mogen meerdere instructies staan; die hoeven niet tussen {} te staan.

3\.  De volgorde van de case- en default-takken mag worden gewijzigd zonder invloed op de uitvoering.

4\.  De default-tak mag worden weggelaten
