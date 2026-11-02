# Fonctions de communication CAN

|                                 |                            |
|---------------------------------|----------------------------|
| **Nom de fonction**             | **Fonction**               |
| **[onCanxStart](#onCanxStart)** | Active la communication CAN |
| **[onCanxstop](#onCanxstop)**   | Arrête la communication CAN |
| **[setBitrate](#setBitrate)**   | Règle la vitesse de communication CAN |
| **[addFillter](#addFillter)**   | Règle le filtre d'ID       |
| **[reciveData](#reciveData)**   | Reçoit des données CAN     |
| **[sendData](#sendData)**       | Envoie des données CAN     |

**1、<span id="onCanxStart"></span>onCanxStart**

**\[Description\]**

Active la communication CAN

Valeur de retour normale = 0, valeur de retour en cas d'erreur &lt;0

**\[Syntaxe\]**

int onCanxStart(PortID);

**\[Exemple\]**

```c
int PortID , Result;
PortID = 0; //0：COM2 1：COM1
Result = 0;
Result = onCanxStart (PortID);
```

**2、<span id="onCanxstop"></span>onCanxstop**

**\[Description\]**

Arrête la communication CAN

Retourne 0 en fonctionnement normal, une valeur non nulle en cas d'erreur

**\[Syntaxe\]**

int onCanxstop (PortID);

**\[Exemple\]**

```c
int PortID , Result;
PortID = 0; //0：COM2 1：COM1
Result = 0;
Result = onCanxstop (PortID);
```

**3、<span id="setBitrate"></span>setBitrate**

**\[Description\]**

Règle la vitesse de communication CAN

Retourne 0 en fonctionnement normal, une valeur non nulle en cas d'erreur

**\[Syntaxe\]**

int setBitrate (PortID);

**\[Exemple\]**

```c
int PortID, Bitrate, Result;
PortID = 0; //0：COM2 1：COM1
Bitrate = 5000; // Vitesse 5K ; plage de réglage 5K, 10K, 20K jusqu'à 1M
Result = 0;
Result = setBitrate ( Bitrate, PortID )// COM0 règle la vitesse de communication à 5000
```

**4、<span id="addFillter"></span>addFillter**

**\[Description\]**

Règle le filtre d'ID

Retourne 0 en fonctionnement normal, une valeur non nulle en cas d'erreur

**\[Syntaxe\]**

int onCanxstop ( CanID, CanMask, PortID );

**\[Exemple\]**

Int PortID, Result, CanID, CanMask;

```c
PortID = 0; //0：COM2 1：COM1
Result = 0;
CanID = 0x11; // ID de début du filtre
CanMask = 0x11; // ID de fin du filtre ; le début et la fin peuvent être identiques
```

Result = onCanxstop ( CanID, CanMask, PortID );   // Ne reçoit que les données d'ID CAN 0x11 ; retourne 0 normalement, une valeur non nulle en cas d'erreur

**5、<span id="reciveData"></span>reciveData**

**\[Description\]**

Reçoit des données CAN

Retourne la longueur des données reçues, une valeur &lt;0 en cas d'erreur

**\[Syntaxe\]**

int reciveData ( data, Len, PortID, &CanID)

**\[Exemple\]**

int PortID, Result, Len;

unsigned data\[128\];        // Tampon de réception

```c
int CanID = 0x00;
PortID = 0; //0：COM2 1：COM1
Len = 128; // Longueur du tampon de réception
Result = reciveData ( ( unsigned char * ) data, Len, PortID ,&CanID);
```

**6、<span id="sendData"></span>sendData**

**\[Description\]**

Envoie des données CAN

Retourne 0 en fonctionnement normal, une valeur non nulle en cas d'erreur

**\[Syntaxe\]**

int sendData ( data, Len, PortID, CanId, CanType )

**\[Exemple\]**

```c
int PortID, Result, Len, CanType, CanId, i;
unsigned char data[128];
PortID = 0; //0：COM2 1：COM1
Result = 0;
Len = 127;
CanId = 0x22;
CanType = 0; // Type de trame : trame standard : 0, trame étendue : 0x80000000
for ( i = 0; i < 128; ++i )
{
data[i] = i;
}
```

Result = sendData ( ( unsigned char \* ) data, Len, PortID, CanId, CanType );// Trame standard, COM0 envoie data, longueur 127, ID CAN 0x22
