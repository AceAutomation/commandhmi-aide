# CAN-Kommunikationsfunktionen

|                                 |                            |
|---------------------------------|----------------------------|
| **Funktionsname**               | **Funktion**               |
| **[onCanxStart](#onCanxStart)** | CAN-Kommunikation starten   |
| **[onCanxstop](#onCanxstop)**   | CAN-Kommunikation beenden    |
| **[setBitrate](#setBitrate)**   | CAN-Baudrate einstellen |
| **[addFillter](#addFillter)**   | ID-Filter setzen          |
| **[reciveData](#reciveData)**   | CAN-Daten empfangen           |
| **[sendData](#sendData)**       | CAN-Daten senden              |

**1、<span id="onCanxStart"></span>onCanxStart**

**\[Beschreibung\]**

CAN-Kommunikation starten

Rückgabewert 0 bei Erfolg, &lt;0 bei Fehler

**\[Verwendung\]**

int onCanxStart(PortID);

**\[Beispiel\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxStart (PortID);
```

**2、<span id="onCanxstop"></span>onCanxstop**

**\[Beschreibung\]**

CAN-Kommunikation beenden

Rückgabewert 0 bei Erfolg, ungleich 0 bei Fehler

**\[Verwendung\]**

int onCanxstop (PortID);

**\[Beispiel\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxstop (PortID);
```

**3、<span id="setBitrate"></span>setBitrate**

**\[Beschreibung\]**

CAN-Baudrate einstellen

Rückgabewert 0 bei Erfolg, ungleich 0 bei Fehler

**\[Verwendung\]**

int setBitrate (PortID);

**\[Beispiel\]**

```c
int PortID, Bitrate, Result;
PortID = 0; //0: COM2 1: COM1
Bitrate = 5000; // Baudrate 5K einstellen; Bereich 5K, 10K, 20K bis maximal 1M
Result = 0;
Result = setBitrate ( Bitrate, PortID )// COM0 stellt die Baudrate auf 5000 ein
```

**4、<span id="addFillter"></span>addFillter**

**\[Beschreibung\]**

ID-Filter setzen

Rückgabewert 0 bei Erfolg, ungleich 0 bei Fehler

**\[Verwendung\]**

int onCanxstop ( CanID, CanMask, PortID );

**\[Beispiel\]**

Int PortID, Result, CanID, CanMask;

```c
PortID = 0; //0: COM2 1: COM1
Result = 0;
CanID = 0x11; // Start-ID des Filters
CanMask = 0x11; // End-ID des Filters; Start und Ende dürfen gleich sein
```

Result = onCanxstop ( CanID, CanMask, PortID );   // Nur Daten mit CAN-ID 0x11 empfangen; Rückgabe 0 bei Erfolg, ungleich 0 bei Fehler

**5、<span id="reciveData"></span>reciveData**

**\[Beschreibung\]**

CAN-Daten empfangen

Rückgabe: Länge der empfangenen Daten bei Erfolg, &lt;0 bei Fehler

**\[Verwendung\]**

int reciveData ( data, Len, PortID, &CanID)

**\[Beispiel\]**

int PortID, Result, Len;

unsigned data\[128\];        // Empfangspuffer

```c
int CanID = 0x00;
PortID = 0; //0: COM2 1: COM1
Len = 128; // Länge des Empfangspuffers
Result = reciveData ( ( unsigned char * ) data, Len, PortID ,&CanID);
```

**6、<span id="sendData"></span>sendData**

**\[Beschreibung\]**

CAN-Daten senden

Rückgabewert 0 bei Erfolg, ungleich 0 bei Fehler

**\[Verwendung\]**

int sendData ( data, Len, PortID, CanId, CanType )

**\[Beispiel\]**

```c
int PortID, Result, Len, CanType, CanId, i;
unsigned char data[128];
PortID = 0; //0: COM2 1: COM1
Result = 0;
Len = 127;
CanId = 0x22;
CanType = 0; // Rahmentyp: Standardrahmen: 0, erweiterter Rahmen: 0x80000000
for ( i = 0; i < 128; ++i )
{
data[i] = i;
}
```

Result = sendData ( ( unsigned char \* ) data, Len, PortID, CanId, CanType );// Standardrahmen, COM0 sendet data, Länge 127, CAN-ID 0x22
