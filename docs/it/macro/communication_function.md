# Funzioni di comunicazione

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
| **Nome funzione** | **Funzione** |
| **[CLEARBUFFER](#CLEARBUFFER)** | Svuota il buffer della porta di comunicazione. |
| **[DELAY](#DELAY)** | Imposta un tempo di ritardo |
| **[FillLW_8](#FillLW_8)** | Scrive dati a 8 bit nei registri LW |
| **[FillLW_16](#FillLW_16)** | Scrive dati a 16 bit nei registri LW. |
| **[FillLW_32](#FillLW_32)** | Scrive dati a 32 bit nei registri LW. |
| **[FillLW_Float](#FillLW_Float)** | Scrive dati float nei registri LW. |
| **[GETCHARS](#GETCHARS)** | Legge i dati dalla porta di comunicazione. |
| **[GETBUFFERLENGTH](#GETBUFFERLENGTH)** | Legge la lunghezza del buffer della porta di comunicazione. |
| **[PUTCHARS](#PUTCHARS)** | Invia dati alla porta di comunicazione. |
| **[InitEthernet](#InitEthernet)** | Modalità client TCP/IP: connessione iniziale. |
| **[readEthernet](#readEthernet)** | Modalità client TCP/IP: lettura dei dati ricevuti. |
| **[writeEthernet](#writeEthernet)** | Modalità client TCP/IP: scrittura dei dati da inviare. |
| **[CountsEthernet](#CountsEthernet)** | Modalità client TCP/IP: numero di byte nel buffer di ricezione; |
| **[ClearEthernet](#ClearEthernet)** | Modalità client TCP/IP: cancella tutti i dati nel buffer di ricezione. |

<span id="CLEARBUFFER"></span>**1、CLEARBUFFER**

**\[Descrizione\]**

Svuota il buffer della porta di comunicazione.

PortID--ID della porta seriale, COM1=0, COM2=1.

Restituisce 1 in caso di successo, 0 in caso di errore.

**\[Sintassi\]**

int CLEARBUFFER(PortID);

**\[Esempio\]**

```c
int Clearresult,PortID;
PortID=0;
Clearresult= CLEARBUFFER(PortID);
```

<span id="DELAY"></span>**2、DELAY**

**\[Descrizione\]**

Imposta un tempo di ritardo;

**\[Sintassi\]**

void DELAY(int dwMilliseconds);

**\[Esempio\]**

```c
int dwMilliseconds=1000;
DELAY(dwMilliseconds);//ritardo di 1 s.
```

<span id="FillLW_8"></span>**3、FillLW_8**

**\[Descrizione\]**

Scrive dati a 8 bit nei registri LW;

**\[Sintassi\]**

```c
FillLW_8(&LocalWord[i],a,NULL,count);
FillLW_8(&LocalWord[i],NULL,a,count);
```

**\[Esempio 1\]**

```c
char a[6]=”arsdw”;
FillLW_8(&LocalWord[6],a,NULL,5);//LW6='a',LW7='r',LW8='s',LW9='d',LW10='w'.
```

**\[Esempio 2\]**

```c
char a[6]={1,2,-1,3,4};
FillLW_8(&LocalWord[6],NULL,a,5);//LW6=1,LW7=2,LW8=-1,LW9=3,LW10=4.
```

<span id="FillLW_16"></span>**4、FillLW_16**

**\[Descrizione\]**

Scrive dati a 16 bit nei registri LW.

**\[Sintassi\]**

```c
FillLW_16(&LocalWord[i],a,NULL,count);
FillLW_16(&LocalWord[i],NULL,a,count);
```

**\[Esempio\]**

```c
short a[6]={12,1,2,-3,4};
unsigned short b[6]={12,5,4,7,8};
FillLW_16(&LocalWord[0],b,NULL,5);//LW0=12,LW1=5,LW2=4,LW3=7,LW4=8.
FillLW_16(&LocalWord[6],NULL,a,5);//LW6=12,LW7=1,LW8=2,LW9=-3,LW10=4.
```

<span id="FillLW_32"></span>**5、FillLW_32**

**\[Descrizione\]**

Scrive dati a 32 bit nei registri LW.

**\[Sintassi\]**

```c
FillLW_32(&LocalWord[i],a,NULL,count);
FillLW_32(&LocalWord[i],NULl,a,count);
```

**\[Esempio\]**

```c
int a[6]={12,1,2,-3,4};
unsigned int b[4]={0x123465,0x541245,0x4444444};
FillLW_32(&LocalWord[0],b,NULL,3);//LW0=1193061,LW2=5509701,LW4=71582788.
FillLW_32(&LocalWord[6],NULL,a,5);//LW6=12,LW8=1,LW10=2,LW12=-3,LW14=4.
```

<span id="FillLW_Float"></span>**6、FillLW_Float**

**\[Descrizione\]**

Scrive dati float nei registri LW.

**\[Sintassi\]**

FillLW_Float(&LocalWord\[i\],source,count)

**\[Esempio\]**

```c
float a[3]={1.2,3.6,4.5};
FillLW_Float(&LocalWord[8],a,3);//LW8=1.2,LW10=3.6,LW12=4.5.
```

<span id="GETCHARS"></span>**7、GETCHARS**

**\[Descrizione\]**

Legge i dati dalla porta di comunicazione.

**\[Sintassi\]**

GETCHARS(PortID, Data)；

**\[Esempio\]**

char Data\[20\]；

int Length,PortID,Result；

```c
Length=5；
PortID=0；
Result=GETCHARS(PortID,Data)；
```

<span id="GETBUFFERLENGTH"></span>**8、GETBUFFERLENGTH**

**\[Descrizione\]**

Legge la lunghezza del buffer della porta di comunicazione.

**\[Sintassi\]**

int GETBUFFERLENGTH(PortID);

**\[Esempio\]**

```c
int bufferlen,PortID;
PortID=0;
bufferlen=GETBUFFERLENGTH(PortID).
```

<span id="PUTCHARS"></span>**9、PUTCHARS**

**\[Descrizione\]**

Invia dati alla porta di comunicazione.

**\[Sintassi\]**

PUTCHARS(PortID, Data, Length)；

**\[Esempio\]**

char Data\[5\] = {0x02, 0x30, 0x31, 0x4d, 0x5e}；

int Length,PortID；

```c
Length=5；
PortID=0；
PUTCHARS(PortID, Data, Length)；
```

<span id="InitEthernet"></span>**10、InitEthernet**

**\[Descrizione\]**

Modalità client TCP/IP: connessione iniziale.

```c
IPAdd--server IP address;
networkPort--connect port number;
```

Restituisce 1 in caso di successo, 0 in caso di errore.

**\[Sintassi\]**

int InitEthernet(char \*IPAdd, int networkPort);

**\[Esempio\]**

```c
char *IPAdd=“192.168.1.100”；
int networkPort=5；
```

int result；

result= InitEthernet(IPAdd, networkPort) ；

<span id="readEthernet"></span>**11、readEthernet**

**\[Descrizione\]**

Modalità client TCP/IP: lettura dei dati ricevuti.

cBuffer--buffer dei dati;

In caso di successo restituisce il numero di byte ricevuti, in caso di errore -1.

**\[Sintassi\]**

int readEthernet(char \*cBuffer);

**\[Esempio\]**

```c
char cBuffer[]={22,33};
int result;
result=readEthernet(cBuffer);
```

<span id="writeEthernet"></span>**12、writeEthernet**

**\[Descrizione\]**

Modalità client TCP/IP: scrittura dei dati da inviare.

```c
cBuffer--data need to send;
iSize--counts need to send;
```

Restituisce 1 in caso di successo, 0 in caso di errore.

**\[Sintassi\]**

int writeEthernet(char \*cBuffer,int isize);

**\[Esempio\]**

```c
char cBuffer[]={22,33};
int isize=8;
int result;
result=writeEthernet(cBuffer,isize);
```

<span id="CountsEthernet"></span>**13、CountsEthernet**

**\[Descrizione\]**

Modalità client TCP/IP: numero di byte nel buffer di ricezione;

In caso di successo restituisce il numero di byte nel buffer di ricezione, in caso di errore 0

**\[Sintassi\]**

int CountsEthernet();

**\[Esempio\]**

```c
int result;
result= CountsEthernet();
```

<span id="ClearEthernet"></span>**14、ClearEthernet**

**\[Descrizione\]**

Modalità client TCP/IP: cancella tutti i dati nel buffer di ricezione.

Restituisce 1 in caso di successo, 0 in caso di errore.

**\[Sintassi\]**

int ClearEthernet();

**\[Esempio\]**

```c
int result;
result= ClearEthernet();
```
