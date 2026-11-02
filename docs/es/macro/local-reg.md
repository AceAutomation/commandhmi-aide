# Uso de la memoria interna en un script

El software de configuración ofrece una interfaz para acceder a la memoria interna del HMI. En un script se puede acceder directamente a la memoria interna de dos maneras:

1.  Acceso a la memoria mediante palabras clave

LocalBit: referencia a la memoria interna LB; LocalWord: referencia a la memoria interna LW; RWIWord: referencia a la memoria interna RWI.

Estas palabras clave pueden usarse directamente en un script. Por ejemplo:

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

2.  Vincular una variable a la memoria interna mediante el ajuste de variables. Véase el uso detallado en el ejemplo de script.
