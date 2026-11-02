# Interne geheugens in een script gebruiken

De configuratiesoftware biedt een interface naar het interne geheugen van de HMI. In een script kan de gebruiker het interne geheugen op twee manieren rechtstreeks gebruiken:

1.  Toegang via sleutelwoorden

LocalBit: verwijst naar het interne geheugen LB; LocalWord: verwijst naar het interne geheugen LW; RWIWord: verwijst naar het interne geheugen RWI.

Het sleutelwoord kan direct in een script worden gebruikt. Bijvoorbeeld:

```c
if(LocalBit[5])
{
LocalWord[1]=0;
}
```

else

```c
{
LocalWord[1]=1;
}
```

2.  Een koppeling tussen een variabele en het interne geheugen leggen via de variabeleninstellingen. Zie het scriptvoorbeeld voor details.
