# Funzioni di comunicazione CAN

|                                 |                            |
|---------------------------------|----------------------------|
| **Nome funzione** | **Funzione** |
| **[onCanxStart](#onCanxStart)** | Attiva la comunicazione CAN |
| **[onCanxstop](#onCanxstop)** | Chiude la comunicazione CAN |
| **[setBitrate](#setBitrate)** | Imposta la velocità di comunicazione CAN |
| **[addFillter](#addFillter)** | Imposta il filtro sugli ID |
| **[reciveData](#reciveData)** | Riceve dati CAN |
| **[sendData](#sendData)** | Invia dati CAN |

**1、<span id="onCanxStart"></span>onCanxStart**

**\[Descrizione\]**

Attiva la comunicazione CAN

Valore restituito: 0 se normale, <0 in caso di errore

**\[Sintassi\]**

int onCanxStart(PortID);

**\[Esempio\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxStart (PortID);
```

**2、<span id="onCanxstop"></span>onCanxstop**

**\[Descrizione\]**

Chiude la comunicazione CAN

Restituisce 0 se normale, un valore diverso da 0 in caso di errore

**\[Sintassi\]**

int onCanxstop (PortID);

**\[Esempio\]**

```c
int PortID , Result;
PortID = 0; //0: COM2 1: COM1
Result = 0;
Result = onCanxstop (PortID);
```

**3、<span id="setBitrate"></span>setBitrate**

**\[Descrizione\]**

Imposta la velocità di comunicazione CAN

Restituisce 0 se normale, un valore diverso da 0 in caso di errore

**\[Sintassi\]**

int setBitrate (PortID);

**\[Esempio\]**

```c
int PortID, Bitrate, Result;
PortID = 0; //0: COM2 1: COM1
Bitrate = 5000; // Imposta la velocità a 5K; valori ammessi 5K, 10K, 20K... fino a un massimo di 1M
Result = 0;
Result = setBitrate ( Bitrate, PortID )// COM0 imposta la velocità di comunicazione a 5000
```

**4、<span id="addFillter"></span>addFillter**

**\[Descrizione\]**

Imposta il filtro sugli ID

Restituisce 0 se normale, un valore diverso da 0 in caso di errore

**\[Sintassi\]**

int onCanxstop ( CanID, CanMask, PortID );

**\[Esempio\]**

Int PortID, Result, CanID, CanMask;

```c
PortID = 0; //0: COM2 1: COM1
Result = 0;
CanID = 0x11; // Imposta l'ID iniziale del filtro
CanMask = 0x11; // Imposta l'ID finale del filtro; iniziale e finale possono coincidere
```

Result = onCanxstop ( CanID, CanMask, PortID );   // Riceve solo i dati con CAN ID 0x11; restituisce 0 se normale, un valore diverso da 0 in caso di errore

**5、<span id="reciveData"></span>reciveData**

**\[Descrizione\]**

Riceve dati CAN

Valore restituito: lunghezza dei dati ricevuti se normale, valore <0 in caso di errore

**\[Sintassi\]**

int reciveData ( data, Len, PortID, &CanID)

**\[Esempio\]**

int PortID, Result, Len;

unsigned data\[128\];        // Buffer dei dati ricevuti

```c
int CanID = 0x00;
PortID = 0; //0: COM2 1: COM1
Len = 128; // Lunghezza del buffer di ricezione
Result = reciveData ( ( unsigned char * ) data, Len, PortID ,&CanID);
```

**6、<span id="sendData"></span>sendData**

**\[Descrizione\]**

Invia dati CAN

Restituisce 0 se normale, un valore diverso da 0 in caso di errore

**\[Sintassi\]**

int sendData ( data, Len, PortID, CanId, CanType )

**\[Esempio\]**

```c
int PortID, Result, Len, CanType, CanId, i;
unsigned char data[128];
PortID = 0; //0: COM2 1: COM1
Result = 0;
Len = 127;
CanId = 0x22;
CanType = 0; // Tipo di frame: frame standard: 0, frame esteso: 0x80000000
for ( i = 0; i < 128; ++i )
{
data[i] = i;
}
```

Result = sendData ( ( unsigned char \* ) data, Len, PortID, CanId, CanType );// Frame standard: COM0 invia data, lunghezza 127, CAN ID 0x22
