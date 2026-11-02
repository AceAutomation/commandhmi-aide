# Fonctions de communication

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
| **Nom de fonction**                     | **Fonction**                                          |
| **[CLEARBUFFER](#CLEARBUFFER)**         | Vide le tampon du port de communication.              |
| **[DELAY](#DELAY)**                     | Définit une temporisation                             |
| **[FillLW_8](#FillLW_8)**               | Écrit des données 8 bits dans les registres LW        |
| **[FillLW_16](#FillLW_16)**             | Écrit des données 16 bits dans les registres LW.      |
| **[FillLW_32](#FillLW_32)**             | Écrit des données 32 bits dans les registres LW.      |
| **[FillLW_Float](#FillLW_Float)**       | Écrit des données flottantes dans les registres LW.   |
| **[GETCHARS](#GETCHARS)**               | Lit des données sur le port de communication.         |
| **[GETBUFFERLENGTH](#GETBUFFERLENGTH)** | Lit la longueur du tampon du port de communication.   |
| **[PUTCHARS](#PUTCHARS)**               | Envoie des données sur le port de communication.      |
| **[InitEthernet](#InitEthernet)**       | Client TCP/IP : connexion initiale.                   |
| **[readEthernet](#readEthernet)**       | Client TCP/IP : lecture des données reçues.           |
| **[writeEthernet](#writeEthernet)**     | Client TCP/IP : écriture des données à envoyer.       |
| **[CountsEthernet](#CountsEthernet)**   | Client TCP/IP : nombre d'octets dans le tampon de réception ; |
| **[ClearEthernet](#ClearEthernet)**     | Client TCP/IP : efface toutes les données du tampon de réception. |

<span id="CLEARBUFFER"></span>**1、CLEARBUFFER**

**\[Description\]**

Vide le tampon du port de communication.

PortID : ID du port série, COM1=0, COM2=1.

Retourne 1 en cas de succès, 0 en cas d'échec.

**\[Syntaxe\]**

int CLEARBUFFER(PortID);

**\[Exemple\]**

```c
int Clearresult,PortID;
PortID=0;
Clearresult= CLEARBUFFER(PortID);
```

<span id="DELAY"></span>**2、DELAY**

**\[Description\]**

Définit une temporisation ;

**\[Syntaxe\]**

void DELAY(int dwMilliseconds);

**\[Exemple\]**

```c
int dwMilliseconds=1000;
DELAY(dwMilliseconds);//Temporisation 1 s.
```

<span id="FillLW_8"></span>**3、FillLW_8**

**\[Description\]**

Écrit des données 8 bits dans les registres LW ;

**\[Syntaxe\]**

```c
FillLW_8(&LocalWord[i],a,NULL,count);
FillLW_8(&LocalWord[i],NULL,a,count);
```

**\[Exemple-1\]**

```c
char a[6]=”arsdw”;
FillLW_8(&LocalWord[6],a,NULL,5);//LW6='a',LW7='r',LW8='s',LW9='d'LW10='w'。
```

**\[Exemple-2\]**

```c
char a[6]={1,2,-1,3,4};
FillLW_8(&LocalWord[6],NULL,a,5);//LW6=1,LW7=2,LW8=-1,LW9=3,LW10=4。
```

<span id="FillLW_16"></span>**4、FillLW_16**

**\[Description\]**

Écrit des données 16 bits dans les registres LW.

**\[Syntaxe\]**

```c
FillLW_16(&LocalWord[i],a,NULL,count);
FillLW_16(&LocalWord[i],NULL,a,count);
```

**\[Exemple\]**

```c
short a[6]={12,1,2,-3,4};
unsigned short b[6]={12,5,4,7,8};
FillLW_16(&LocalWord[0],b,NULL,5);//LW0=12,LW1=5,LW2=4,LW3=7,LW4=8。
FillLW_16(&LocalWord[6],NULL,a,5);//LW6=12,LW7=1,LW8=2,LW9=-3,LW10=4。
```

<span id="FillLW_32"></span>**5、FillLW_32**

**\[Description\]**

Écrit des données 32 bits dans les registres LW.

**\[Syntaxe\]**

```c
FillLW_32(&LocalWord[i],a,NULL,count);
FillLW_32(&LocalWord[i],NULl,a,count);
```

**\[Exemple\]**

```c
int a[6]={12,1,2,-3,4};
unsigned int b[4]={0x123465,0x541245,0x4444444};
FillLW_32(&LocalWord[0],b,NULL,3);//LW0=1193061,LW2=5509701,LW4=71582788。
FillLW_32(&LocalWord[6],NULL,a,5);//LW6=12,LW8=1,LW10=2,LW12=-3,LW14=4。
```

<span id="FillLW_Float"></span>**6、FillLW_Float**

**\[Description\]**

Écrit des données flottantes dans les registres LW.

**\[Syntaxe\]**

FillLW_Float(&LocalWord\[i\],source,count)

**\[Exemple\]**

```c
float a[3]={1.2,3.6,4.5};
FillLW_Float(&LocalWord[8],a,3);//LW8=1.2,LW10=3.6,LW12=4.5。
```

<span id="GETCHARS"></span>**7、GETCHARS**

**\[Description\]**

Lit des données sur le port de communication.

**\[Syntaxe\]**

GETCHARS(PortID, Data)；

**\[Exemple\]**

char Data\[20\]；

int Length,PortID,Result；

```c
Length=5；
PortID=0；
Result=GETCHARS(PortID,Data)；
```

<span id="GETBUFFERLENGTH"></span>**8、GETBUFFERLENGTH**

**\[Description\]**

Lit la longueur du tampon du port de communication.

**\[Syntaxe\]**

int GETBUFFERLENGTH(PortID);

**\[Exemple\]**

```c
int bufferlen,PortID;
PortID=0;
bufferlen=GETBUFFERLENGTH(PortID).
```

<span id="PUTCHARS"></span>**9、PUTCHARS**

**\[Description\]**

Envoie des données sur le port de communication.

**\[Syntaxe\]**

PUTCHARS(PortID, Data, Length)；

**\[Exemple\]**

char Data\[5\] = {0x02, 0x30, 0x31, 0x4d, 0x5e}；

int Length,PortID；

```c
Length=5；
PortID=0；
PUTCHARS(PortID, Data, Length)；
```

<span id="InitEthernet"></span>**10、InitEthernet**

**\[Description\]**

Client TCP/IP : connexion initiale.

```c
IPAdd--server IP address;
networkPort--connect port number;
```

Retourne 1 en cas de succès, 0 en cas d'échec.

**\[Syntaxe\]**

int InitEthernet(char \*IPAdd, int networkPort);

**\[Exemple\]**

```c
char *IPAdd=“192.168.1.100”；
int networkPort=5；
```

int result；

result= InitEthernet(IPAdd, networkPort) ；

<span id="readEthernet"></span>**11、readEthernet**

**\[Description\]**

Client TCP/IP : lecture des données reçues.

cBuffer : tampon de données ;

Retourne le nombre d'octets reçus en cas de succès, -1 en cas d'échec.

**\[Syntaxe\]**

int readEthernet(char \*cBuffer);

**\[Exemple\]**

```c
char cBuffer[]={22,33};
int result;
result=readEthernet(cBuffer);
```

<span id="writeEthernet"></span>**12、writeEthernet**

**\[Description\]**

Client TCP/IP : écriture des données à envoyer.

```c
cBuffer--data need to send;
iSize--counts need to send;
```

Retourne 1 en cas de succès, 0 en cas d'échec.

**\[Syntaxe\]**

int writeEthernet(char \*cBuffer,int isize);

**\[Exemple\]**

```c
char cBuffer[]={22,33};
int isize=8;
int result;
result=writeEthernet(cBuffer,isize);
```

<span id="CountsEthernet"></span>**13、CountsEthernet**

**\[Description\]**

Client TCP/IP : nombre d'octets dans le tampon de réception ;

Retourne le nombre d'octets du tampon de réception en cas de succès, 0 en cas d'échec

**\[Syntaxe\]**

int CountsEthernet();

**\[Exemple\]**

```c
int result;
result= CountsEthernet();
```

<span id="ClearEthernet"></span>**14、ClearEthernet**

**\[Description\]**

Client TCP/IP : efface toutes les données du tampon de réception.

Retourne 1 en cas de succès, 0 en cas d'échec.

**\[Syntaxe\]**

int ClearEthernet();

**\[Exemple\]**

```c
int result;
result= ClearEthernet();
```
