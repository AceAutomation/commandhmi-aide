# Utiliser la mémoire interne dans les scripts

Le logiciel de configuration donne accès à la mémoire interne de l'IHM : les scripts peuvent agir directement sur cette mémoire. Deux méthodes sont possibles :

1.  Accès à la mémoire par mots-clés

LocalBit : référence à la zone mémoire interne LB ; LocalWord : référence à la zone LW ; RWIWord : référence à la zone RWI.

Ces mots-clés s'utilisent directement dans les macros. Par exemple :

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

2.  Liaison entre une variable et la mémoire interne par le réglage des variables. Pour le détail, voir l'exemple de script.
