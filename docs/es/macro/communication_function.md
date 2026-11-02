# Funciones de comunicación

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
| **Nombre de la función**                       | **Función**                                          |
| **[CLEARBUFFER](#CLEARBUFFER)**         | Vacía el búfer del puerto de comunicación.                   |
| **[DELAY](#DELAY)**                     | Define un tiempo de espera                                    |
| **[FillLW_8](#FillLW_8)**               | Escribe datos de 8 bits en registros LW                       |
| **[FillLW_16](#FillLW_16)**             | Escribe datos de 16 bits en registros LW.                     |
| **[FillLW_32](#FillLW_32)**             | Escribe datos de 32 bits en registros LW.                     |
| **[FillLW_Float](#FillLW_Float)**       | Escribe datos de coma flotante en registros LW.                      |
| **[GETCHARS](#GETCHARS)**               | Lee datos del puerto de comunicación.                     |
| **[GETBUFFERLENGTH](#GETBUFFERLENGTH)** | Lee la longitud del búfer del puerto de comunicación.            |
| **[PUTCHARS](#PUTCHARS)**               | Envía datos al puerto de comunicación.                      |
| **[InitEthernet](#InitEthernet)**       | Cliente TCP/IP: establece la conexión.                   |
| **[readEthernet](#readEthernet)**       | Cliente TCP/IP: lee los datos recibidos.                 |
| **[writeEthernet](#writeEthernet)**     | Cliente TCP/IP: escribe los datos a enviar.                   |
| **[CountsEthernet](#CountsEthernet)**   | Cliente TCP/IP: cantidad de datos en el búfer de recepción;          |
| **[ClearEthernet](#ClearEthernet)**     | Cliente TCP/IP: borra todos los datos del búfer de recepción. |

<span id="CLEARBUFFER"></span>**1、CLEARBUFFER**

**\[Descripción\]**

Vacía el búfer del puerto de comunicación.

PortID: ID del puerto serie, COM1=0, COM2=1.

Devuelve 1 si la operación tiene éxito y 0 si falla.

**\[Uso\]**

int CLEARBUFFER(PortID);

**\[Ejemplo\]**

```c
int Clearresult,PortID;
PortID=0;
Clearresult= CLEARBUFFER(PortID);
```

<span id="DELAY"></span>**2、DELAY**

**\[Descripción\]**

Define un tiempo de espera;

**\[Uso\]**

void DELAY(int dwMilliseconds);

**\[Ejemplo\]**

```c
int dwMilliseconds=1000;
DELAY(dwMilliseconds);//Retardo de 1 s.
```

<span id="FillLW_8"></span>**3、FillLW_8**

**\[Descripción\]**

Escribe datos de 8 bits en registros LW;

**\[Uso\]**

```c
FillLW_8(&LocalWord[i],a,NULL,count);
FillLW_8(&LocalWord[i],NULL,a,count);
```

**\[Ejemplo 1\]**

```c
char a[6]=”arsdw”;
FillLW_8(&LocalWord[6],a,NULL,5);//LW6='a',LW7='r',LW8='s',LW9='d'LW10='w'。
```

**\[Ejemplo 2\]**

```c
char a[6]={1,2,-1,3,4};
FillLW_8(&LocalWord[6],NULL,a,5);//LW6=1,LW7=2,LW8=-1,LW9=3,LW10=4。
```

<span id="FillLW_16"></span>**4、FillLW_16**

**\[Descripción\]**

Escribe datos de 16 bits en registros LW.

**\[Uso\]**

```c
FillLW_16(&LocalWord[i],a,NULL,count);
FillLW_16(&LocalWord[i],NULL,a,count);
```

**\[Ejemplo\]**

```c
short a[6]={12,1,2,-3,4};
unsigned short b[6]={12,5,4,7,8};
FillLW_16(&LocalWord[0],b,NULL,5);//LW0=12,LW1=5,LW2=4,LW3=7,LW4=8。
FillLW_16(&LocalWord[6],NULL,a,5);//LW6=12,LW7=1,LW8=2,LW9=-3,LW10=4。
```

<span id="FillLW_32"></span>**5、FillLW_32**

**\[Descripción\]**

Escribe datos de 32 bits en registros LW.

**\[Uso\]**

```c
FillLW_32(&LocalWord[i],a,NULL,count);
FillLW_32(&LocalWord[i],NULl,a,count);
```

**\[Ejemplo\]**

```c
int a[6]={12,1,2,-3,4};
unsigned int b[4]={0x123465,0x541245,0x4444444};
FillLW_32(&LocalWord[0],b,NULL,3);//LW0=1193061,LW2=5509701,LW4=71582788。
FillLW_32(&LocalWord[6],NULL,a,5);//LW6=12,LW8=1,LW10=2,LW12=-3,LW14=4。
```

<span id="FillLW_Float"></span>**6、FillLW_Float**

**\[Descripción\]**

Escribe datos de coma flotante en registros LW.

**\[Uso\]**

FillLW_Float(&LocalWord\[i\],source,count)

**\[Ejemplo\]**

```c
float a[3]={1.2,3.6,4.5};
FillLW_Float(&LocalWord[8],a,3);//LW8=1.2,LW10=3.6,LW12=4.5。
```

<span id="GETCHARS"></span>**7、GETCHARS**

**\[Descripción\]**

Lee datos del puerto de comunicación.

**\[Uso\]**

GETCHARS(PortID, Data)；

**\[Ejemplo\]**

char Data\[20\]；

int Length,PortID,Result；

```c
Length=5；
PortID=0；
Result=GETCHARS(PortID,Data)；
```

<span id="GETBUFFERLENGTH"></span>**8、GETBUFFERLENGTH**

**\[Descripción\]**

Lee la longitud del búfer del puerto de comunicación.

**\[Uso\]**

int GETBUFFERLENGTH(PortID);

**\[Ejemplo\]**

```c
int bufferlen,PortID;
PortID=0;
bufferlen=GETBUFFERLENGTH(PortID).
```

<span id="PUTCHARS"></span>**9、PUTCHARS**

**\[Descripción\]**

Envía datos al puerto de comunicación.

**\[Uso\]**

PUTCHARS(PortID, Data, Length)；

**\[Ejemplo\]**

char Data\[5\] = {0x02, 0x30, 0x31, 0x4d, 0x5e}；

int Length,PortID；

```c
Length=5；
PortID=0；
PUTCHARS(PortID, Data, Length)；
```

<span id="InitEthernet"></span>**10、InitEthernet**

**\[Descripción\]**

Cliente TCP/IP: establece la conexión.

```c
IPAdd--server IP address;
networkPort--connect port number;
```

Devuelve 1 si tiene éxito y 0 si falla.

**\[Uso\]**

int InitEthernet(char \*IPAdd, int networkPort);

**\[Ejemplo\]**

```c
char *IPAdd=“192.168.1.100”；
int networkPort=5；
```

int result；

result= InitEthernet(IPAdd, networkPort) ；

<span id="readEthernet"></span>**11、readEthernet**

**\[Descripción\]**

Cliente TCP/IP: lee los datos recibidos.

cBuffer: búfer de datos;

Devuelve el número de datos recibidos si tiene éxito y -1 si falla.

**\[Uso\]**

int readEthernet(char \*cBuffer);

**\[Ejemplo\]**

```c
char cBuffer[]={22,33};
int result;
result=readEthernet(cBuffer);
```

<span id="writeEthernet"></span>**12、writeEthernet**

**\[Descripción\]**

Cliente TCP/IP: escribe los datos a enviar.

```c
cBuffer--data need to send;
iSize--counts need to send;
```

Devuelve 1 si tiene éxito y 0 si falla.

**\[Uso\]**

int writeEthernet(char \*cBuffer,int isize);

**\[Ejemplo\]**

```c
char cBuffer[]={22,33};
int isize=8;
int result;
result=writeEthernet(cBuffer,isize);
```

<span id="CountsEthernet"></span>**13、CountsEthernet**

**\[Descripción\]**

Cliente TCP/IP: cantidad de datos en el búfer de recepción;

Devuelve la cantidad de datos del búfer de recepción si tiene éxito y 0 si falla

**\[Uso\]**

int CountsEthernet();

**\[Ejemplo\]**

```c
int result;
result= CountsEthernet();
```

<span id="ClearEthernet"></span>**14、ClearEthernet**

**\[Descripción\]**

Cliente TCP/IP: borra todos los datos del búfer de recepción.

Devuelve 1 si tiene éxito y 0 si falla.

**\[Uso\]**

int ClearEthernet();

**\[Ejemplo\]**

```c
int result;
result= ClearEthernet();
```
