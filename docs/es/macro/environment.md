# Ejemplo de protocolo de comunicación libre (Free Port)

Ajustes de los parámetros de comunicación libre, como abajo:

<img src="../../macro/environment.files/image001.jpg" width="601" alt="ScreenShot00094.jpg" />

El puerto COM se ajusta a Samkoon – NULL PLC

Los parámetros de comunicación por defecto son los siguientes:

<img src="../../macro/environment.files/image002.jpg" width="595" alt="ScreenShot00095.jpg" />

Primero, cree tres pantallas:

<img src="../../macro/environment.files/environment42.png" width="800" />

Pantalla 1

<img src="../../macro/environment.files/environment61.png" width="793" />

Pantalla 2

<img src="../../macro/environment.files/environment80.png" width="809" />

Pantalla 3

Los seis objetos de la derecha de las pantallas 1 y 3 son visualizaciones numéricas cuyas direcciones de monitorización son, de arriba abajo, LW60297, LW60298, LW60299, LW60300, LW60301 y LW60302 = 1. Los dos objetos rojos son lámparas de bit con las direcciones LB100 y LB101. Los objetos de abajo de la pantalla 3 son visualizaciones numéricas a partir de la dirección LW400, con un intervalo de 1.

Ajustes «Avanzado» de los dos botones de pantalla de la pantalla 2:

<img src="../../macro/environment.files/environment619.png" width="675" />

<img src="../../macro/environment.files/environment621.png" width="675" />

Ajuste del script global:

<img src="../../macro/environment.files/environment646.png" width="437" />

<img src="../../macro/environment.files/environment648.png" width="437" />

**Código de Marco_COM:**

```c
#include "MacroInit.h"
void Macro_main(IN *p)
{
```

MarcoInit

```c
LW60297=0;
LW60298=3;
LW60299=0;
LW60300=1;
LW60302=1;
char Pdata[20];
char Gdata[100];
int result;
if (LB0==0) // 0: estado de envío; 1: estado de espera de recepción
{
Pdata[0]=LW200;
Pdata[1]=LW201;
Pdata[2]=LW202;
Pdata[3]=LW203;
PUTCHARS(0,Pdata,4);
LB0=1; //
return; //
}
```

else

```c
{
result=GETCHARS(0,Gdata);
LW0=result;
if (result<=0) // 0: sin recepción; 1: recepción errónea
{
LW1++; // tiempo de espera agotado, empieza el recuento
if (LW1>=3) // esperar el tiempo de 3 ejecuciones del script
{
LW1=0; // puesta a cero
LB0=0; // enviar la marca de puesta a cero; se enviará la próxima vez
}
return; // salir directamente
}
else // recepción correcta
{
LW2=Gdata[0]&0xff; // tratamiento de los datos recibidos
LW3=Gdata[1]&0xff;
LW4=Gdata[2];
LW5=Gdata[3];
LB0=0; // tratamiento terminado; se enviará en la próxima entrada
PUTCHARS(0,Pdata,0); //vaciar el búfer
}
}
}
```

**Código de Macro1:**

```c
#include "MacroInit.h"
void Macro_main(IN *p)
{
```

MarcoInit

```c
LW60297=0;
LW60298=4;
LW60299=0;
LW60300=1;
LW60302=2;
char Pdata[20]; //array de datos enviados
char Mdata[100]; //array de datos recibidos
int result; //longitud de los datos de respuesta recibidos
if (LB0==0) //LB0 es la marca de envío/recepción: 0 estado de envío, 1 estado de espera de recepción
{
Pdata[0]=0x02; //enviar datos, leer los registros de retención; el primer byte es la dirección del esclavo
Pdata[1]=0x03; //código de función: lectura de registros de retención
Pdata[2]=0x00; // dirección inicial de los datos a leer
Pdata[3]=0x00;
Pdata[4]=0x00; //número de palabras a leer
Pdata[5]=0x03;
Wcrc=CRC(Pdata,6); //CRC de los datos anteriores
Pdata[6]=(Wcrc&0xff); //intercambio alto/bajo del CRC; P6 toma el byte bajo
Pdata[7]=(Wcrc>>8); //P7 toma el byte alto
PUTCHARS(0,Pdata,8); //función de envío; envía todos los datos al puerto serie
LB0=1; // envío terminado; en la próxima entrada se espera la recepción en lugar de enviar
return; //salir y esperar la recepción
}
```

else

```c
{
result=GETCHARS(0,Mdata);//función de recepción; guarda los datos recibidos en el array Gdata
LW0=result; //comprobar la longitud recibida
if (result<=0) //0: sin recepción; 1: recepción errónea
{
LW1++; //tiempo de espera agotado; empieza el recuento
if (LW1>=3) //esperar el tiempo de 3 ejecuciones del script
{
LW1=0; //puesta a cero
LB0=0; //enviar la marca de puesta a cero; se enviará en la próxima entrada
}
return; //salir directamente
}
else //recepción correcta
{
LW400=Mdata[0]&0xff; //tratamiento de los datos recibidos
LW401=Mdata[1]&0xff;
LW402=Mdata[2];
LW403=Mdata[3];
LW404=Mdata[4];
LW405=Mdata[5];
LW406=Mdata[6];
LW407=Mdata[7];
LW408=Mdata[8];
LW409=Mdata[9];
LW410=Mdata[10];
LB0=0; //tratamiento terminado; se enviará en la próxima entrada
PUTCHARS(0,Pdata,0); //vaciar el búfer
}
}
}
```

<img src="../../macro/environment.files/environment3382.png" width="130" />

El nombre y la dirección de las variables son los mismos en la ventana de compilación.
