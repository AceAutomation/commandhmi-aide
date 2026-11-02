# Kommunikationsfunktionen

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
| **Funktionsname**                       | **Funktion**                                          |
| **[CLEARBUFFER](#CLEARBUFFER)**         | Leert den Puffer der Kommunikationsschnittstelle.                   |
| **[DELAY](#DELAY)**                     | Legt eine Verzögerungszeit fest                                    |
| **[FillLW_8](#FillLW_8)**               | Schreibt 8-Bit-Daten in LW-Register                       |
| **[FillLW_16](#FillLW_16)**             | Schreibt 16-Bit-Daten in LW-Register.                     |
| **[FillLW_32](#FillLW_32)**             | Schreibt 32-Bit-Daten in LW-Register.                     |
| **[FillLW_Float](#FillLW_Float)**       | Schreibt Gleitkommadaten in LW-Register.                      |
| **[GETCHARS](#GETCHARS)**               | Liest Daten von der Kommunikationsschnittstelle.                     |
| **[GETBUFFERLENGTH](#GETBUFFERLENGTH)** | Liest die Pufferlänge der Kommunikationsschnittstelle.            |
| **[PUTCHARS](#PUTCHARS)**               | Sendet Daten an die Kommunikationsschnittstelle.                      |
| **[InitEthernet](#InitEthernet)**       | TCP/IP-Client: Verbindung aufbauen.                   |
| **[readEthernet](#readEthernet)**       | TCP/IP-Client: empfangene Daten lesen.                 |
| **[writeEthernet](#writeEthernet)**     | TCP/IP-Client: Sendedaten schreiben.                   |
| **[CountsEthernet](#CountsEthernet)**   | TCP/IP-Client: Anzahl der Daten im Empfangspuffer;          |
| **[ClearEthernet](#ClearEthernet)**     | TCP/IP-Client: löscht alle Daten im Empfangspuffer. |

<span id="CLEARBUFFER"></span>**1、CLEARBUFFER**

**\[Beschreibung\]**

Leert den Puffer der Kommunikationsschnittstelle.

PortID – ID der seriellen Schnittstelle, COM1=0, COM2=1.

Rückgabewert 1 bei Erfolg, 0 bei Fehler.

**\[Verwendung\]**

int CLEARBUFFER(PortID);

**\[Beispiel\]**

```c
int Clearresult,PortID;
PortID=0;
Clearresult= CLEARBUFFER(PortID);
```

<span id="DELAY"></span>**2、DELAY**

**\[Beschreibung\]**

Legt eine Verzögerungszeit fest;

**\[Verwendung\]**

void DELAY(int dwMilliseconds);

**\[Beispiel\]**

```c
int dwMilliseconds=1000;
DELAY(dwMilliseconds);//1 s Verzögerung.
```

<span id="FillLW_8"></span>**3、FillLW_8**

**\[Beschreibung\]**

Schreibt 8-Bit-Daten in LW-Register;

**\[Verwendung\]**

```c
FillLW_8(&LocalWord[i],a,NULL,count);
FillLW_8(&LocalWord[i],NULL,a,count);
```

**\[Beispiel 1\]**

```c
char a[6]=”arsdw”;
FillLW_8(&LocalWord[6],a,NULL,5);//LW6='a',LW7='r',LW8='s',LW9='d'LW10='w'。
```

**\[Beispiel 2\]**

```c
char a[6]={1,2,-1,3,4};
FillLW_8(&LocalWord[6],NULL,a,5);//LW6=1,LW7=2,LW8=-1,LW9=3,LW10=4。
```

<span id="FillLW_16"></span>**4、FillLW_16**

**\[Beschreibung\]**

Schreibt 16-Bit-Daten in LW-Register.

**\[Verwendung\]**

```c
FillLW_16(&LocalWord[i],a,NULL,count);
FillLW_16(&LocalWord[i],NULL,a,count);
```

**\[Beispiel\]**

```c
short a[6]={12,1,2,-3,4};
unsigned short b[6]={12,5,4,7,8};
FillLW_16(&LocalWord[0],b,NULL,5);//LW0=12,LW1=5,LW2=4,LW3=7,LW4=8。
FillLW_16(&LocalWord[6],NULL,a,5);//LW6=12,LW7=1,LW8=2,LW9=-3,LW10=4。
```

<span id="FillLW_32"></span>**5、FillLW_32**

**\[Beschreibung\]**

Schreibt 32-Bit-Daten in LW-Register.

**\[Verwendung\]**

```c
FillLW_32(&LocalWord[i],a,NULL,count);
FillLW_32(&LocalWord[i],NULl,a,count);
```

**\[Beispiel\]**

```c
int a[6]={12,1,2,-3,4};
unsigned int b[4]={0x123465,0x541245,0x4444444};
FillLW_32(&LocalWord[0],b,NULL,3);//LW0=1193061,LW2=5509701,LW4=71582788。
FillLW_32(&LocalWord[6],NULL,a,5);//LW6=12,LW8=1,LW10=2,LW12=-3,LW14=4。
```

<span id="FillLW_Float"></span>**6、FillLW_Float**

**\[Beschreibung\]**

Schreibt Gleitkommadaten in LW-Register.

**\[Verwendung\]**

FillLW_Float(&LocalWord\[i\],source,count)

**\[Beispiel\]**

```c
float a[3]={1.2,3.6,4.5};
FillLW_Float(&LocalWord[8],a,3);//LW8=1.2,LW10=3.6,LW12=4.5。
```

<span id="GETCHARS"></span>**7、GETCHARS**

**\[Beschreibung\]**

Liest Daten von der Kommunikationsschnittstelle.

**\[Verwendung\]**

GETCHARS(PortID, Data)；

**\[Beispiel\]**

char Data\[20\]；

int Length,PortID,Result；

```c
Length=5；
PortID=0；
Result=GETCHARS(PortID,Data)；
```

<span id="GETBUFFERLENGTH"></span>**8、GETBUFFERLENGTH**

**\[Beschreibung\]**

Liest die Pufferlänge der Kommunikationsschnittstelle.

**\[Verwendung\]**

int GETBUFFERLENGTH(PortID);

**\[Beispiel\]**

```c
int bufferlen,PortID;
PortID=0;
bufferlen=GETBUFFERLENGTH(PortID).
```

<span id="PUTCHARS"></span>**9、PUTCHARS**

**\[Beschreibung\]**

Sendet Daten an die Kommunikationsschnittstelle.

**\[Verwendung\]**

PUTCHARS(PortID, Data, Length)；

**\[Beispiel\]**

char Data\[5\] = {0x02, 0x30, 0x31, 0x4d, 0x5e}；

int Length,PortID；

```c
Length=5；
PortID=0；
PUTCHARS(PortID, Data, Length)；
```

<span id="InitEthernet"></span>**10、InitEthernet**

**\[Beschreibung\]**

TCP/IP-Client: Verbindung aufbauen.

```c
IPAdd--server IP address;
networkPort--connect port number;
```

Rückgabewert 1 bei Erfolg, 0 bei Fehler.

**\[Verwendung\]**

int InitEthernet(char \*IPAdd, int networkPort);

**\[Beispiel\]**

```c
char *IPAdd=“192.168.1.100”；
int networkPort=5；
```

int result；

result= InitEthernet(IPAdd, networkPort) ；

<span id="readEthernet"></span>**11、readEthernet**

**\[Beschreibung\]**

TCP/IP-Client: empfangene Daten lesen.

cBuffer – Datenpuffer;

Rückgabe: Anzahl der empfangenen Daten bei Erfolg, -1 bei Fehler.

**\[Verwendung\]**

int readEthernet(char \*cBuffer);

**\[Beispiel\]**

```c
char cBuffer[]={22,33};
int result;
result=readEthernet(cBuffer);
```

<span id="writeEthernet"></span>**12、writeEthernet**

**\[Beschreibung\]**

TCP/IP-Client: Sendedaten schreiben.

```c
cBuffer--data need to send;
iSize--counts need to send;
```

Rückgabewert 1 bei Erfolg, 0 bei Fehler.

**\[Verwendung\]**

int writeEthernet(char \*cBuffer,int isize);

**\[Beispiel\]**

```c
char cBuffer[]={22,33};
int isize=8;
int result;
result=writeEthernet(cBuffer,isize);
```

<span id="CountsEthernet"></span>**13、CountsEthernet**

**\[Beschreibung\]**

TCP/IP-Client: Anzahl der Daten im Empfangspuffer;

Rückgabe: Anzahl der Daten im Empfangspuffer bei Erfolg, 0 bei Fehler

**\[Verwendung\]**

int CountsEthernet();

**\[Beispiel\]**

```c
int result;
result= CountsEthernet();
```

<span id="ClearEthernet"></span>**14、ClearEthernet**

**\[Beschreibung\]**

TCP/IP-Client: löscht alle Daten im Empfangspuffer.

Rückgabewert 1 bei Erfolg, 0 bei Fehler.

**\[Verwendung\]**

int ClearEthernet();

**\[Beispiel\]**

```c
int result;
result= ClearEthernet();
```
