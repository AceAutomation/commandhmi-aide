# Programma's met lussen

De lus is een belangrijke programmastructuur. Zolang aan een voorwaarde is voldaan, wordt een programmadeel herhaald, tot de voorwaarde niet meer geldt. De voorwaarde heet de lusvoorwaarde, het herhaalde deel de lusbody. C biedt meerdere lusinstructies waarmee verschillende lusstructuren kunnen worden gemaakt.

**1.  while-instructie**

Algemene vorm van de while-instructie: while (expressie) instructie;

Daarbij is de expressie de lusvoorwaarde en de instructie de lusbody.

Betekenis van de while-instructie: de expressie wordt geëvalueerd; zolang ze waar is (niet 0), wordt de lusbody uitgevoerd.

Aandachtspunten bij de while-instructie:

1\.  De expressie van while is meestal een relationele of logische expressie. Zolang ze waar is (niet 0), gaat de lus verder.

2\.  Bestaat de lusbody uit meer dan één instructie, dan moet die tussen {} staan als samengestelde instructie.

3\.  Let op de lusvoorwaarde om oneindige lussen te vermijden.

**2.  do-while-instructie**

Algemene vorm van de do-while-instructie:

```c
do statement;
while (expression);
```

Daarbij is de instructie de lusbody en de expressie de lusvoorwaarde. Betekenis van de do-while-instructie:

Eerst wordt de lusbody één keer uitgevoerd en daarna de expressie geëvalueerd. Is die waar (niet 0), dan gaat de lus verder; anders eindigt ze.

Het verschil tussen do-while en while is dat do-while eerst uitvoert en daarna test; de lusbody wordt dus minstens één keer uitgevoerd. while test eerst en voert daarna uit: is de voorwaarde niet vervuld, dan wordt de lusbody geen enkele keer uitgevoerd.

while- en do-while-instructies zijn meestal in elkaar om te schrijven.

In dit voorbeeld is de lusvoorwaarde herschreven tot –n; anders zou de lus één keer te veel worden doorlopen. Aandachtspunten bij de do-while-instructie:

1\.  Bij if en while staat na de expressie geen puntkomma; bij do-while moet de expressie met een puntkomma eindigen.

2\.  do-while-instructies kunnen geneste lussen vormen en met while-instructies worden gecombineerd.

3\.  Bestaat de lusbody tussen do en while uit meerdere instructies, dan moeten die tussen {} staan als samengestelde instructie.

4\.  Pas bij het omzetten van do-while naar while en omgekeerd de lusvoorwaarde aan.
