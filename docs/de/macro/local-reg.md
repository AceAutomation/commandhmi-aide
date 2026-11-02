# Internen Speicher in Skripten verwenden

Die Projektierungssoftware bietet Zugriff auf den internen Speicher des HMI; Skripte können direkt darauf zugreifen. Zwei Methoden sind möglich:

1.  Zugriff über Schlüsselwörter

LocalBit: Zugriff auf den internen Bereich LB; LocalWord: Zugriff auf den internen Bereich LW; RWIWord: Zugriff auf den internen Bereich RWI.

Diese Schlüsselwörter lassen sich direkt in Skripten verwenden. Beispiel:

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

2.  Verknüpfung einer Variablen mit dem internen Speicher über die Variableneinstellungen. Einzelheiten siehe Skriptbeispiel.
