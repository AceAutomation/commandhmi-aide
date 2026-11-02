# Communicatiefuncties

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
| **Functienaam**                       | **Functie**                                          |
| **[CLEARBUFFER](#CLEARBUFFER)**         | Maakt de buffer van de communicatiepoort leeg.                   |
| **[DELAY](#DELAY)**                     | Stelt een wachttijd in                                    |
| **[FillLW_8](#FillLW_8)**               | Schrijft 8-bits gegevens naar LW-registers                       |
| **[FillLW_16](#FillLW_16)**             | Schrijft 16-bits gegevens naar LW-registers.                     |
| **[FillLW_32](#FillLW_32)**             | Schrijft 32-bits gegevens naar LW-registers.                     |
| **[FillLW_Float](#FillLW_Float)**       | Schrijft drijvendekommagegevens naar LW-registers.                      |
| **[GETCHARS](#GETCHARS)**               | Leest gegevens van de communicatiepoort.                     |
| **[GETBUFFERLENGTH](#GETBUFFERLENGTH)** | Leest de bufferlengte van de communicatiepoort.            |
| **[PUTCHARS](#PUTCHARS)**               | Verzendt gegevens naar de communicatiepoort.                      |
| **[InitEthernet](#InitEthernet)**       | TCP/IP-client: verbinding maken.                   |
| **[readEthernet](#readEthernet)**       | TCP/IP-client: ontvangen gegevens lezen.                 |
| **[writeEthernet](#writeEthernet)**     | TCP/IP-client: te verzenden gegevens schrijven.                   |
| **[CountsEthernet](#CountsEthernet)**   | TCP/IP-client: aantal gegevens in de ontvangstbuffer;          |
| **[ClearEthernet](#ClearEthernet)**     | TCP/IP-client: wist alle gegevens in de ontvangstbuffer. |

<span id="CLEARBUFFER"></span>**1、CLEARBUFFER**

**\[Beschrijving\]**

Wist de buffer van de communicatiepoort.

PortID: ID van de seriële poort, COM1=0, COM2=1.

Retourneert 1 bij succes en 0 bij een fout.

**\[Gebruik\]**

int CLEARBUFFER(PortID);

**\[Voorbeeld\]**

```c
int Clearresult,PortID;
PortID=0;
Clearresult= CLEARBUFFER(PortID);
```

<span id="DELAY"></span>**2、DELAY**

**\[Beschrijving\]**

Stelt een vertraging in;

**\[Gebruik\]**

void DELAY(int dwMilliseconds);

**\[Voorbeeld\]**

```c
int dwMilliseconds=1000;
DELAY(dwMilliseconds);//Vertraging van 1 s.
```

<span id="FillLW_8"></span>**3、FillLW_8**

**\[Beschrijving\]**

Schrijft 8-bits gegevens naar LW-registers;

**\[Gebruik\]**

```c
FillLW_8(&LocalWord[i],a,NULL,count);
FillLW_8(&LocalWord[i],NULL,a,count);
```

**\[Voorbeeld 1\]**

```c
char a[6]=”arsdw”;
FillLW_8(&LocalWord[6],a,NULL,5);//LW6='a',LW7='r',LW8='s',LW9='d'LW10='w'。
```

**\[Voorbeeld 2\]**

```c
char a[6]={1,2,-1,3,4};
FillLW_8(&LocalWord[6],NULL,a,5);//LW6=1,LW7=2,LW8=-1,LW9=3,LW10=4。
```

<span id="FillLW_16"></span>**4、FillLW_16**

**\[Beschrijving\]**

Schrijft 16-bits gegevens naar LW-registers.

**\[Gebruik\]**

```c
FillLW_16(&LocalWord[i],a,NULL,count);
FillLW_16(&LocalWord[i],NULL,a,count);
```

**\[Voorbeeld\]**

```c
short a[6]={12,1,2,-3,4};
unsigned short b[6]={12,5,4,7,8};
FillLW_16(&LocalWord[0],b,NULL,5);//LW0=12,LW1=5,LW2=4,LW3=7,LW4=8。
FillLW_16(&LocalWord[6],NULL,a,5);//LW6=12,LW7=1,LW8=2,LW9=-3,LW10=4。
```

<span id="FillLW_32"></span>**5、FillLW_32**

**\[Beschrijving\]**

Schrijft 32-bits gegevens naar LW-registers.

**\[Gebruik\]**

```c
FillLW_32(&LocalWord[i],a,NULL,count);
FillLW_32(&LocalWord[i],NULl,a,count);
```

**\[Voorbeeld\]**

```c
int a[6]={12,1,2,-3,4};
unsigned int b[4]={0x123465,0x541245,0x4444444};
FillLW_32(&LocalWord[0],b,NULL,3);//LW0=1193061,LW2=5509701,LW4=71582788。
FillLW_32(&LocalWord[6],NULL,a,5);//LW6=12,LW8=1,LW10=2,LW12=-3,LW14=4。
```

<span id="FillLW_Float"></span>**6、FillLW_Float**

**\[Beschrijving\]**

Schrijft floatgegevens naar LW-registers.

**\[Gebruik\]**

FillLW_Float(&LocalWord\[i\],source,count)

**\[Voorbeeld\]**

```c
float a[3]={1.2,3.6,4.5};
FillLW_Float(&LocalWord[8],a,3);//LW8=1.2,LW10=3.6,LW12=4.5。
```

<span id="GETCHARS"></span>**7、GETCHARS**

**\[Beschrijving\]**

Leest gegevens van de communicatiepoort.

**\[Gebruik\]**

GETCHARS(PortID, Data)；

**\[Voorbeeld\]**

char Data\[20\]；

int Length,PortID,Result；

```c
Length=5；
PortID=0；
Result=GETCHARS(PortID,Data)；
```

<span id="GETBUFFERLENGTH"></span>**8、GETBUFFERLENGTH**

**\[Beschrijving\]**

Leest de bufferlengte van de communicatiepoort.

**\[Gebruik\]**

int GETBUFFERLENGTH(PortID);

**\[Voorbeeld\]**

```c
int bufferlen,PortID;
PortID=0;
bufferlen=GETBUFFERLENGTH(PortID).
```

<span id="PUTCHARS"></span>**9、PUTCHARS**

**\[Beschrijving\]**

Verzendt gegevens naar de communicatiepoort.

**\[Gebruik\]**

PUTCHARS(PortID, Data, Length)；

**\[Voorbeeld\]**

char Data\[5\] = {0x02, 0x30, 0x31, 0x4d, 0x5e}；

int Length,PortID；

```c
Length=5；
PortID=0；
PUTCHARS(PortID, Data, Length)；
```

<span id="InitEthernet"></span>**10、InitEthernet**

**\[Beschrijving\]**

TCP/IP-clientmodus: verbinding initialiseren.

```c
IPAdd--server IP address;
networkPort--connect port number;
```

Retourneert 1 bij succes, 0 bij een fout.

**\[Gebruik\]**

int InitEthernet(char \*IPAdd, int networkPort);

**\[Voorbeeld\]**

```c
char *IPAdd=“192.168.1.100”；
int networkPort=5；
```

int result；

result= InitEthernet(IPAdd, networkPort) ；

<span id="readEthernet"></span>**11、readEthernet**

**\[Beschrijving\]**

TCP/IP-clientmodus: ontvangen gegevens lezen.

cBuffer: gegevensbuffer;

Retourneert het aantal ontvangen bytes, -1 bij een fout.

**\[Gebruik\]**

int readEthernet(char \*cBuffer);

**\[Voorbeeld\]**

```c
char cBuffer[]={22,33};
int result;
result=readEthernet(cBuffer);
```

<span id="writeEthernet"></span>**12、writeEthernet**

**\[Beschrijving\]**

TCP/IP-clientmodus: gegevens verzenden.

```c
cBuffer--data need to send;
iSize--counts need to send;
```

Retourneert 1 bij succes, 0 bij een fout.

**\[Gebruik\]**

int writeEthernet(char \*cBuffer,int isize);

**\[Voorbeeld\]**

```c
char cBuffer[]={22,33};
int isize=8;
int result;
result=writeEthernet(cBuffer,isize);
```

<span id="CountsEthernet"></span>**13、CountsEthernet**

**\[Beschrijving\]**

TCP/IP-clientmodus: aantal bytes in de ontvangstbuffer;

Retourneert het aantal bytes in de ontvangstbuffer, 0 bij een fout

**\[Gebruik\]**

int CountsEthernet();

**\[Voorbeeld\]**

```c
int result;
result= CountsEthernet();
```

<span id="ClearEthernet"></span>**14、ClearEthernet**

**\[Beschrijving\]**

TCP/IP-clientmodus: alle gegevens in de ontvangstbuffer wissen.

Retourneert 1 bij succes, 0 bij een fout.

**\[Gebruik\]**

int ClearEthernet();

**\[Voorbeeld\]**

```c
int result;
result= ClearEthernet();
```
