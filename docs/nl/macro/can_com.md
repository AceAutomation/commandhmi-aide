# CAN-communicatiefuncties

|                                 |                            |
|---------------------------------|----------------------------|
| **Functienaam**               | **Functie**               |
| **[onCanxStart](#onCanxStart)** | CAN-communicatie openen   |
| **[onCanxstop](#onCanxstop)**   | CAN-communicatie sluiten    |
| **[setBitrate](#setBitrate)**   | CAN-baudrate instellen |
| **[addFillter](#addFillter)**   | ID-filter instellen          |
| **[reciveData](#reciveData)**   | CAN-gegevens ontvangen           |
| **[sendData](#sendData)**       | CAN-gegevens verzenden              |

**1、<span id="onCanxStart"></span>onCanxStart**

**\[Beschrijving\]**

Schakelt de CAN-communicatie in

Retourwaarde 0 = OK, foutwaarde &lt;0

**\[Gebruik\]**

int onCanxStart(PortID);

**\[Voorbeeld\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxStart (PortID);
```

**2、<span id="onCanxstop"></span>onCanxstop**

**\[Beschrijving\]**

Schakelt de CAN-communicatie uit

Retourwaarde 0 = OK, anders fout

**\[Gebruik\]**

int onCanxstop (PortID);

**\[Voorbeeld\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxstop (PortID);
```

**3、<span id="setBitrate"></span>setBitrate**

**\[Beschrijving\]**

Stelt de CAN-communicatiesnelheid in

Retourwaarde 0 = OK, anders fout

**\[Gebruik\]**

int setBitrate (PortID);

**\[Voorbeeld\]**

```c
int PortID, Bitrate, Result;
PortID = 0; //0: COM2 1: COM1
Bitrate = 5000; // Baudrate 5K; instelbereik 5K, 10K, 20K tot maximaal 1M
Result = 0;
Result = setBitrate ( Bitrate, PortID )// COM0: communicatiesnelheid 5000
```

**4、<span id="addFillter"></span>addFillter**

**\[Beschrijving\]**

Stelt het ID-filter in

Retourwaarde 0 = OK, anders fout

**\[Gebruik\]**

int onCanxstop ( CanID, CanMask, PortID );

**\[Voorbeeld\]**

Int PortID, Result, CanID, CanMask;

```c
PortID = 0; //0: COM2 1: COM1
Result = 0;
CanID = 0x11; // Eerste ID van het filter
CanMask = 0x11; // Laatste ID van het filter; begin en einde mogen gelijk zijn
```

Result = onCanxstop ( CanID, CanMask, PortID );   // Alleen gegevens met CAN ID 0x11 ontvangen; retourwaarde 0 = OK, anders fout

**5、<span id="reciveData"></span>reciveData**

**\[Beschrijving\]**

Ontvangt CAN-gegevens

Retourwaarde: lengte van de ontvangen gegevens; bij een fout &lt;0

**\[Gebruik\]**

int reciveData ( data, Len, PortID, &CanID)

**\[Voorbeeld\]**

int PortID, Result, Len;

unsigned data\[128\];        // Ontvangstbuffer

```c
int CanID = 0x00;
PortID = 0; //0: COM2 1: COM1
Len = 128; // Lengte van de ontvangstbuffer
Result = reciveData ( ( unsigned char * ) data, Len, PortID ,&CanID);
```

**6、<span id="sendData"></span>sendData**

**\[Beschrijving\]**

Verzendt CAN-gegevens

Retourwaarde 0 = OK, anders fout

**\[Gebruik\]**

int sendData ( data, Len, PortID, CanId, CanType )

**\[Voorbeeld\]**

```c
int PortID, Result, Len, CanType, CanId, i;
unsigned char data[128];
PortID = 0; //0: COM2 1: COM1
Result = 0;
Len = 127;
CanId = 0x22;
CanType = 0; // Frametype: standaardframe 0, uitgebreid frame 0x80000000
for ( i = 0; i < 128; ++i )
{
data[i] = i;
}
```

Result = sendData ( ( unsigned char \* ) data, Len, PortID, CanId, CanType );// Standaardframe, COM0 verzendt data, lengte 127, CAN ID 0x22
