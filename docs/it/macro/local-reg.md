# Uso dell'area di memoria interna negli script

Il software di configurazione SKTOOL offre un'interfaccia per operare sull'area di memoria interna dell'HMI. L'utente può operare direttamente sull'area di memoria interna nello script, in due modi:

1.  Accesso all'area di memoria tramite parole chiave

LocalBit: riferimento all'area di memoria interna LB; LocalWord: riferimento all'area di memoria interna LW; RWIWord: riferimento all'area di memoria interna RWI.

Le parole chiave possono essere usate direttamente nella macro. Per esempio:

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

2.  Si stabilisce un collegamento tra la variabile e l'area di memoria interna tramite l'impostazione delle variabili. Per l'uso dettagliato, vedere l'esempio di script.
