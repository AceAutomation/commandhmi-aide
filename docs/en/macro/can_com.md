# CAN communication function

|                                 |                            |
|---------------------------------|----------------------------|
| **Function name**               | **Function**               |
| **[onCanxStart](#onCanxStart)** | Enable CAN communication   |
| **[onCanxstop](#onCanxstop)**   | Close CAN communication    |
| **[setBitrate](#setBitrate)**   | Set CAN communication rate |
| **[addFillter](#addFillter)**   | Set the ID filter          |
| **[reciveData](#reciveData)**   | Receive CAN data           |
| **[sendData](#sendData)**       | Send CAN data              |

**1、<span id="onCanxStart"></span>onCanxStart**

**\[Description\]**

Enable CAN communication

Normal return value =0, error return value &lt;0

**\[Usage\]**

int onCanxStart(PortID);

**\[Example\]**

```c
int PortID , Result;
PortID = 0; //0：COM2 1：COM1
Result = 0;
Result = onCanxStart (PortID);
```

**2、<span id="onCanxstop"></span>onCanxstop**

**\[Description\]**

Close CAN communication

Normal returns 0, error returns non-0

**\[Usage\]**

int onCanxstop (PortID);

**\[Example\]**

```c
int PortID , Result;
PortID = 0; //0：COM2 1：COM1
Result = 0;
Result = onCanxstop (PortID);
```

**3、<span id="setBitrate"></span>setBitrate**

**\[Description\]**

Set CAN communication rate

Normal returns 0, error returns non-0

**\[Usage\]**

int setBitrate (PortID);

**\[Example\]**

```c
int PortID, Bitrate, Result;
PortID = 0; //0：COM2 1：COM1
Bitrate = 5000; // Set the baud rate 5K set range 5K 10K 20K maximum to 1M
Result = 0;
Result = setBitrate ( Bitrate, PortID )// COM0 sets the communication rate to 5000
```

**4、<span id="addFillter"></span>addFillter**

**\[Description\]**

Set the ID filter

Normal returns 0, error returns non-0

**\[Usage\]**

int onCanxstop ( CanID, CanMask, PortID );

**\[Example\]**

Int PortID, Result, CanID, CanMask;

```c
PortID = 0; //0：COM2 1：COM1
Result = 0;
CanID = 0x11; // Set the filter start ID number
CanMask = 0x11; // Set the filter end ID number, and start and end can be the same
```

Result = onCanxstop ( CanID, CanMask, PortID );   // Set to receive only data with CAN ID 0x11 normally returns 0 error returns non-0 value

**5、<span id="reciveData"></span>reciveData**

**\[Description\]**

Receive CAN data

Normal return received data length, error return data length &lt;0

**\[Usage\]**

int reciveData ( data, Len, PortID, &CanID)

**\[Example\]**

int PortID, Result, Len;

unsigned data\[128\];        // Receive data buffer

```c
int CanID = 0x00;
PortID = 0; //0：COM2 1：COM1
Len = 128; // Receive buffer length
Result = reciveData ( ( unsigned char * ) data, Len, PortID ,&CanID);
```

**6、<span id="sendData"></span>sendData**

**\[Description\]**

Send CAN data

Normal returns 0, error returns non-0

**\[Usage\]**

int sendData ( data, Len, PortID, CanId, CanType )

**\[Example\]**

```c
int PortID, Result, Len, CanType, CanId, i;
unsigned char data[128];
PortID = 0; //0：COM2 1：COM1
Result = 0;
Len = 127;
CanId = 0x22;
CanType = 0; // Frame type: standard frame: 0 extended frame:0x80000000
for ( i = 0; i < 128; ++i )
{
data[i] = i;
}
```

Result = sendData ( ( unsigned char \* ) data, Len, PortID, CanId, CanType );// Standard frame, COM0 sends data data, length 127,CAN ID 0x22
