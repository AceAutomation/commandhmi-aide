# Communication function

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
| **Function name**                       | **function**                                          |
| **[CLEARBUFFER](#CLEARBUFFER)**         | Clear buffer of communication port.                   |
| **[DELAY](#DELAY)**                     | Set a delayed time                                    |
| **[FillLW_8](#FillLW_8)**               | Give 8-bit dates to LW register                       |
| **[FillLW_16](#FillLW_16)**             | Give 16-bit dates to LW register.                     |
| **[FillLW_32](#FillLW_32)**             | Give 32-bit dates to LW register.                     |
| **[FillLW_Float](#FillLW_Float)**       | Give float dates to LW register.                      |
| **[GETCHARS](#GETCHARS)**               | Get data from communication port.                     |
| **[GETBUFFERLENGTH](#GETBUFFERLENGTH)** | Get buffer length from communication port.            |
| **[PUTCHARS](#PUTCHARS)**               | Send data to communication port.                      |
| **[InitEthernet](#InitEthernet)**       | TCP/IP client mode initial connect.                   |
| **[readEthernet](#readEthernet)**       | TCP/IP client mode read receive data.                 |
| **[writeEthernet](#writeEthernet)**     | TCP/IP client mode write send data.                   |
| **[CountsEthernet](#CountsEthernet)**   | TCP/IP client mode counts in receive buffer;          |
| **[ClearEthernet](#ClearEthernet)**     | TCP/IP client mode delete all data in receive buffer. |

<span id="CLEARBUFFER"></span>**1、CLEARBUFFER**

**\[Description\]**

Clear buffer of communication port.

PortID--串口ID,COM1=0, COM2=1。

操作成功返回 1, 失败返回 0。

**\[Usage\]**

int CLEARBUFFER(PortID);

**\[Example\]**

```c
int Clearresult,PortID;
PortID=0;
Clearresult= CLEARBUFFER(PortID);
```

<span id="DELAY"></span>**2、DELAY**

**\[Description\]**

Set a delayed time；

**\[Usage\]**

void DELAY(int dwMilliseconds);

**\[Example\]**

```c
int dwMilliseconds=1000;
DELAY(dwMilliseconds);//延迟1s.
```

<span id="FillLW_8"></span>**3、FillLW_8**

**\[Description\]**

Give 8-bit dates to LW register;

**\[Usage\]**

```c
FillLW_8(&LocalWord[i],a,NULL,count);
FillLW_8(&LocalWord[i],NULL,a,count);
```

**\[Example-1\]**

```c
char a[6]=”arsdw”;
FillLW_8(&LocalWord[6],a,NULL,5);//LW6='a',LW7='r',LW8='s',LW9='d'LW10='w'。
```

**\[Example-2\]**

```c
char a[6]={1,2,-1,3,4};
FillLW_8(&LocalWord[6],NULL,a,5);//LW6=1,LW7=2,LW8=-1,LW9=3,LW10=4。
```

<span id="FillLW_16"></span>**4、FillLW_16**

**\[Description\]**

Give 16-bit dates to LW register.

**\[Usage\]**

```c
FillLW_16(&LocalWord[i],a,NULL,count);
FillLW_16(&LocalWord[i],NULL,a,count);
```

**\[Example\]**

```c
short a[6]={12,1,2,-3,4};
unsigned short b[6]={12,5,4,7,8};
FillLW_16(&LocalWord[0],b,NULL,5);//LW0=12,LW1=5,LW2=4,LW3=7,LW4=8。
FillLW_16(&LocalWord[6],NULL,a,5);//LW6=12,LW7=1,LW8=2,LW9=-3,LW10=4。
```

<span id="FillLW_32"></span>**5、FillLW_32**

**\[Description\]**

Give 32-bit dates to LW register.

**\[Usage\]**

```c
FillLW_32(&LocalWord[i],a,NULL,count);
FillLW_32(&LocalWord[i],NULl,a,count);
```

**\[Example\]**

```c
int a[6]={12,1,2,-3,4};
unsigned int b[4]={0x123465,0x541245,0x4444444};
FillLW_32(&LocalWord[0],b,NULL,3);//LW0=1193061,LW2=5509701,LW4=71582788。
FillLW_32(&LocalWord[6],NULL,a,5);//LW6=12,LW8=1,LW10=2,LW12=-3,LW14=4。
```

<span id="FillLW_Float"></span>**6、FillLW_Float**

**\[Description\]**

Give float dates to LW register.

**\[Usage\]**

FillLW_Float(&LocalWord\[i\],source,count)

**\[Example\]**

```c
float a[3]={1.2,3.6,4.5};
FillLW_Float(&LocalWord[8],a,3);//LW8=1.2,LW10=3.6,LW12=4.5。
```

<span id="GETCHARS"></span>**7、GETCHARS**

**\[Description\]**

Get data from communication port.

**\[Usage\]**

GETCHARS(PortID, Data)；

**\[Example\]**

char Data\[20\]；

int Length,PortID,Result；

```c
Length=5；
PortID=0；
Result=GETCHARS(PortID,Data)；
```

<span id="GETBUFFERLENGTH"></span>**8、GETBUFFERLENGTH**

**\[Description\]**

Get buffer length from communication port.

**\[Usage\]**

int GETBUFFERLENGTH(PortID);

**\[Example\]**

```c
int bufferlen,PortID;
PortID=0;
bufferlen=GETBUFFERLENGTH(PortID).
```

<span id="PUTCHARS"></span>**9、PUTCHARS**

**\[Description\]**

Send data to communication port.

**\[Usage\]**

PUTCHARS(PortID, Data, Length)；

**\[Example\]**

char Data\[5\] = {0x02, 0x30, 0x31, 0x4d, 0x5e}；

int Length,PortID；

```c
Length=5；
PortID=0；
PUTCHARS(PortID, Data, Length)；
```

<span id="InitEthernet"></span>**10、InitEthernet**

**\[Description\]**

TCP/IP client mode initial connect.

```c
IPAdd--server IP address;
networkPort--connect port number;
```

Success return 1, fail return 0.

**\[Usage\]**

int InitEthernet(char \*IPAdd, int networkPort);

**\[Example\]**

```c
char *IPAdd=“192.168.1.100”；
int networkPort=5；
```

int result；

result= InitEthernet(IPAdd, networkPort) ；

<span id="readEthernet"></span>**11、readEthernet**

**\[Description\]**

TCP/IP client mode read receive data.

cBuffer--data buffer;

Success return receive counts, fail return -1.

**\[Usage\]**

int readEthernet(char \*cBuffer);

**\[Example\]**

```c
char cBuffer[]={22,33};
int result;
result=readEthernet(cBuffer);
```

<span id="writeEthernet"></span>**12、writeEthernet**

**\[Description\]**

TCP/IP client mode write send data.

```c
cBuffer--data need to send;
iSize--counts need to send;
```

Success return 1, fail return 0.

**\[Usage\]**

int writeEthernet(char \*cBuffer,int isize);

**\[Example\]**

```c
char cBuffer[]={22,33};
int isize=8;
int result;
result=writeEthernet(cBuffer,isize);
```

<span id="CountsEthernet"></span>**13、CountsEthernet**

**\[Description\]**

TCP/IP client mode counts in receive buffer;

Success return counts in receive buffer, fail return 0

**\[Usage\]**

int CountsEthernet();

**\[Example\]**

```c
int result;
result= CountsEthernet();
```

<span id="ClearEthernet"></span>**14、ClearEthernet**

**\[Description\]**

TCP/IP client mode delete all data in receive buffer.

Success return 1, fail return 0.

**\[Usage\]**

int ClearEthernet();

**\[Example\]**

```c
int result;
result= ClearEthernet();
```
