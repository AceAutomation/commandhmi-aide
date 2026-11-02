# Funciones de comunicación CAN

|                                 |                            |
|---------------------------------|----------------------------|
| **Nombre de la función**               | **Función**               |
| **[onCanxStart](#onCanxStart)** | Abrir la comunicación CAN   |
| **[onCanxstop](#onCanxstop)**   | Cerrar la comunicación CAN    |
| **[setBitrate](#setBitrate)**   | Ajustar la velocidad CAN |
| **[addFillter](#addFillter)**   | Ajustar el filtro de ID          |
| **[reciveData](#reciveData)**   | Recibir datos CAN           |
| **[sendData](#sendData)**       | Enviar datos CAN              |

**1、<span id="onCanxStart"></span>onCanxStart**

**\[Descripción\]**

Abre la comunicación CAN

Devuelve 0 si es correcto y un valor &lt;0 en caso de error

**\[Uso\]**

int onCanxStart(PortID);

**\[Ejemplo\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxStart (PortID);
```

**2、<span id="onCanxstop"></span>onCanxstop**

**\[Descripción\]**

Cierra la comunicación CAN

Devuelve 0 si es correcto y un valor distinto de 0 en caso de error

**\[Uso\]**

int onCanxstop (PortID);

**\[Ejemplo\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxstop (PortID);
```

**3、<span id="setBitrate"></span>setBitrate**

**\[Descripción\]**

Ajusta la velocidad de comunicación CAN

Devuelve 0 si es correcto y un valor distinto de 0 en caso de error

**\[Uso\]**

int setBitrate (PortID);

**\[Ejemplo\]**

```c
int PortID, Bitrate, Result;
PortID = 0; //0: COM2 1: COM1
Bitrate = 5000; // Velocidad de 5K; rango de 5K, 10K, 20K hasta 1M
Result = 0;
Result = setBitrate ( Bitrate, PortID )// COM0: velocidad de comunicación 5000
```

**4、<span id="addFillter"></span>addFillter**

**\[Descripción\]**

Ajusta el filtro de ID

Devuelve 0 si es correcto y un valor distinto de 0 en caso de error

**\[Uso\]**

int onCanxstop ( CanID, CanMask, PortID );

**\[Ejemplo\]**

Int PortID, Result, CanID, CanMask;

```c
PortID = 0; //0: COM2 1: COM1
Result = 0;
CanID = 0x11; // ID inicial del filtro
CanMask = 0x11; // ID final del filtro; el inicial y el final pueden ser iguales
```

Result = onCanxstop ( CanID, CanMask, PortID );   // Solo se reciben los datos con CAN ID 0x11; devuelve 0 si es correcto y un valor distinto de 0 en caso de error

**5、<span id="reciveData"></span>reciveData**

**\[Descripción\]**

Recibe datos CAN

Devuelve la longitud de los datos recibidos si es correcto, y una longitud &lt;0 en caso de error

**\[Uso\]**

int reciveData ( data, Len, PortID, &CanID)

**\[Ejemplo\]**

int PortID, Result, Len;

unsigned data\[128\];        // Búfer de recepción

```c
int CanID = 0x00;
PortID = 0; //0: COM2 1: COM1
Len = 128; // Longitud del búfer de recepción
Result = reciveData ( ( unsigned char * ) data, Len, PortID ,&CanID);
```

**6、<span id="sendData"></span>sendData**

**\[Descripción\]**

Envía datos CAN

Devuelve 0 si es correcto y un valor distinto de 0 en caso de error

**\[Uso\]**

int sendData ( data, Len, PortID, CanId, CanType )

**\[Ejemplo\]**

```c
int PortID, Result, Len, CanType, CanId, i;
unsigned char data[128];
PortID = 0; //0: COM2 1: COM1
Result = 0;
Len = 127;
CanId = 0x22;
CanType = 0; // Tipo de trama: trama estándar: 0, trama extendida: 0x80000000
for ( i = 0; i < 128; ++i )
{
data[i] = i;
}
```

Result = sendData ( ( unsigned char \* ) data, Len, PortID, CanId, CanType );// Trama estándar, COM0 envía los datos data, longitud 127, CAN ID 0x22
