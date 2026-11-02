# Driver per dispositivi Siemens

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Questo driver permette agli HMI serie HM di leggere e scrivere dati o stati dei registri dei PLC Siemens serie S7-200/300/1200. La comunicazione avviene tra la porta del touch screen e quella del PLC Siemens serie S7-200/300/1200tcp. Prima di usare il driver, leggere attentamente questo capitolo e le specifiche tecniche del PLC Siemens serie S7-200/300/1200tcp.</p></td>
</tr>
<tr class="even">
<td><p> Come collegare un PLC Siemens serie S7-200/300/1200tcp</p>
<p><strong>1.1 Collegamento hardware</strong></p>
<p>Cavo di collegamento:</p>
<p>RS485-Siemens S7-200<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p>Siemens serie S7-200</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>8</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>3</p></td>
<td><p>TX+</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/siemens.files/image002.gif" width="130" /><img src="../../drivers/siemens.files/image003.gif" width="290" /><img src="../../drivers/siemens.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

  RS232-Siemens S7-300

|                             |     |                           |     |
|-----------------------------|-----|---------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Siemens serie S7-300** |     |
| **2**                       | RX  | 3                         | TX  |
| **3**                       | TX  | 2                         | RX  |
| **5**                       | GND | 5                         | GND |

|     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |
|     | <img src="../../drivers/siemens.files/image005.gif" width="408" /> |     | <img src="../../drivers/siemens.files/image006.gif" width="129" /> |

Il connettore dell'HMI è DB9F, quello della porta MPI del PLC Siemens serie S7-300 è DB9M.

Come collegare un PLC Siemens serie S7-200/300/1200

**1.2 Collegamento hardware**

Cavo di collegamento:

  Cavo RJ45;

  Piedinatura RJ45:

**<img src="../../drivers/siemens.files/image014.jpg" width="343" />**

1. Impostazione di IP e numero di porta

Nella scheda General delle proprietà della porta di comunicazione, selezionare "Ethernet Port" come interfaccia di collegamento e "SIEMENS", "Siemens S7-200(TCP/IP)/Siemens S7-300(TCP/IP)/Siemens S7-1200(TCP)" come servizio di collegamento;

Nella scheda Parameter delle proprietà della porta di comunicazione, impostare IP e numero di porta.

Attenzione:

L'indirizzo IP del PLC deve trovarsi nella stessa sottorete dell'HMI: basta impostare la subnet mask a 255.255.255.0.

2. Nelle impostazioni del PLC Siemens 1200 occorre verificare se è attiva la protezione dell'accesso; se necessario, selezionare l'opzione indicata, quindi ricompilare e scaricare il programma nel PLC.

In TIA Portal, caricare il programma del PLC o crearne uno nuovo per S7-1200; fare clic con il tasto destro sul dispositivo e selezionare "Properties"; in "Protection" selezionare "Permit access with PUT/GET communication from remote partner (PLC, HMI, OPC...)", come mostrato nella figura seguente:

**<img src="../../drivers/siemens.files/image015.jpg" width="1152" />**

**2. Impostazioni software**

Selezionare SIEMENS nel servizio del dispositivo collegato.

Selezionare la voce corrispondente nel servizio del dispositivo collegato in base al modello di PLC o al protocollo supportato.

Verificare che i parametri di comunicazione del touch screen e il numero di stazione del PLC corrispondano a quelli del PLC collegato.

Per le impostazioni del PLC, consultare la documentazione tecnica del PLC Siemens serie S7-200/300

Parametri di collegamento predefiniti degli HMI serie HM

|                             |                         |                                    |                                              |
|-----------------------------|-------------------------|------------------------------------|----------------------------------------------|
| **Parametro** | Valore predefinito |                                    | Valori ammessi |
| **Tipo di PLC** | S7-200(PPI) |                                    | S7-200(PPI)/ S7-300(MPI) |
| **Tipo di porta di comunicazione** | RS485 |                                    | RS232/RS422/RS485 |
| **Velocità (baud)** | 19200 |                                    | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bit di dati** | 8 |                                    | 7/8 |
| **Parità** | EVEN |                                    | EVEN/ODD/NONE |
| **Bit di stop** | 1 |                                    | 1/2 |
| **Numero di stazione PLC** | 2 |                                    | da 1 a 255 |
| **Numero di stazione HMI** | 0 |                                    | da 0 a 255 |
| **Funzione** |                         | **Supportata** |                                              |
| **Simulazione offline** |                         | Sì |                                              |
| **Simulazione online** |                         | Sì |                                              |
| **Modalità estesa** |                         | Sì: S7-200(PPI) / No: S7-300(MPI) |                                              |
|                             |                         |                                    |                                              |

**3. Registri utilizzabili e intervalli di indirizzi**

Siemens S7-200

|                   |                    |                 |                                                                                                    |
|-------------------|--------------------|-----------------|----------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | dd.o | da 0.0 a 4095.7 | Bit: immagine degli ingressi, sola lettura |
| **Q** | dd.o | da 0.0 a 4095.7 | Bit: immagine delle uscite |
| **M** | dd.o | da 0.0 a 4095.7 | Bit: memoria a bit (merker) |
| **S** | dd.o | da 0.0 a 4095.7 | Bit: relè di controllo sequenziale |
| **SM** | ddd.o | da 0.0 a 4095.7 | Bit: memoria speciale, SM0.0-SM29.7 sola lettura |
| **T** | ddd | da 0 a 255 | Bit: stato del timer, sola lettura |
| **C** | ddd | da 0 a 255 | Bit: stato del contatore, sola lettura |
| **VB_Bit** | ddddd.o | da 0.0 a 10239.7 | Bit: bit della memoria variabili |
| **IW** | dd | da 0 a 4095 | Word: immagine degli ingressi, sola lettura, registro a 8 bit, ogni word occupa due indirizzi |
| **QW** | dd | da 0 a 4095 | Word: immagine delle uscite, registro a 8 bit, ogni word occupa due indirizzi |
| **MW** | dd | da 0 a 4095 | Word: memoria a bit (merker), registro a 8 bit, ogni word occupa due indirizzi |
| **SW** | dd | da 0 a 4095 | Word: relè di controllo sequenziale, registro a 8 bit, ogni word occupa due indirizzi |
| **SMW** | ddd | da 0 a 4095 | Word: memoria speciale, SMW0-SMW29 sola lettura, registro a 8 bit, ogni word occupa due indirizzi |
| **VB** | ddddd | da 0 a 10239 | Word: memoria variabili, registro a 8 bit |
| **VW** | ddddd | da 0 a 10238 | Word: memoria variabili, registro a 8 bit, ogni word occupa due indirizzi |
| **VD** | ddddd | da 0 a 10236 | Double word: memoria variabili, registro a 8 bit, ogni double word occupa quattro indirizzi |
| **TV** | ddd | da 0 a 255 | Word: valore corrente del timer |
| **CV** | ddd | da 0 a 255 | Word: valore corrente del contatore |
| **AIW** | dd | da 0 a 62 | Word: ingresso analogico, sola lettura, registro a 8 bit, ogni word occupa due indirizzi |
| **AQW** | dd | da 0 a 62 | Word: uscita analogica, sola scrittura, registro a 8 bit, ogni word occupa due indirizzi |

Siemens S7-300 / Siemens S7-300(MPI) / Siemens S7-300tcp

|                   |                    |                     |                                                                                                                                                            |
|-------------------|--------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | dddd.o | da 0.0 a 4095.7 | Bit: immagine degli ingressi |
| **Q** | dddd.o | da 0.0 a 4095.7 | Bit: immagine delle uscite |
| **M** | dddd.o | da 0.0 a 4095.7 | Bit: memoria a bit (merker) |
| **DB_Bit** | DDD:dddd.o | da 0:0.0 a 255:8192.7 | Bit: bit di una word di un blocco dati DB; numero di blocco DDD da 0 a 255, word dddd da 0 a 8192, bit o da 0 a 7 |
| **IW** | dddd | da 0 a 4095 | Word: immagine degli ingressi, registro a 8 bit, ogni word occupa due indirizzi |
| **QW** | dddd | da 0 a 4095 | Word: immagine delle uscite, registro a 8 bit, ogni word occupa due indirizzi |
| **MW** | dddd | da 0 a 4095 | Word: memoria a bit (merker), registro a 8 bit, ogni word occupa due indirizzi |
| **DBW** | DDD:dddd | da 0:0 a 255:8192 | Word: blocco dati DB; numero di blocco DDD da 0 a 255, word dddd da 0 a 8192, registro a 8 bit, ogni word occupa due indirizzi |
| **DBD** | DDD:dddd | da 0:0 a 255:8192 | Double word: blocco dati DB; numero di blocco DDD da 0 a 255, word dddd da 0 a 8192, registro a 8 bit, ogni double word occupa quattro indirizzi |

Siemens S7-1200tcp

|                   |                    |                  |                                                                                                                                                            |
|-------------------|--------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | dddd.o | 0.0~1024.7 | Bit: immagine degli ingressi |
| **Q** | dddd.o | 0.0~1024.7 | Bit: immagine delle uscite |
| **M** | dddd.o | 0.0~8191.7 | Bit: memoria a bit (merker) |
| **DB_Bit** | DDD:dddd.o | 0:0.0~255:8192.7 | Bit: bit di una word di un blocco dati DB; numero di blocco DDD da 0 a 255, word dddd da 0 a 8192, bit o da 0 a 7 |
| **IW** | dddd | 0~1024 | Word: immagine degli ingressi, registro a 8 bit, ogni word occupa due indirizzi |
| **QW** | dddd | 0~1024 | Word: immagine delle uscite, registro a 8 bit, ogni word occupa due indirizzi |
| **MW** | dddd | 0~8191 | Word: memoria a bit (merker), registro a 8 bit, ogni word occupa due indirizzi |
| **DBW** | DDD:dddd | 0:0~255:8192 | Word: blocco dati DB; numero di blocco DDD da 0 a 255, word dddd da 0 a 8192, registro a 8 bit, ogni word occupa due indirizzi |
| **DBD** | DDD:dddd | 0:0~255:8192 | Double word: blocco dati DB; numero di blocco DDD da 0 a 255, word dddd da 0 a 8192, registro a 8 bit, ogni double word occupa quattro indirizzi |

LOGO_TCP

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nome registro** | **Formato indirizzo** | **Intervallo** | **Note** |
| **I** | dd | 1~64 | Bit: immagine degli ingressi |
| **Q** | dd | 1~64 | Bit: immagine delle uscite |
| **M** | ddd | 1~112 | Bit: memoria a bit (merker) |
| **VB**            | dddd.o             | 0.0~1023.7      | Bit                            |
| **AI** | dd | 1~16 | Word: ingressi analogici |
| **AQ** | dd | 1~16 | Word: uscite analogiche |
| **AM** | dd | 1~64 | Word: merker analogici |
| **VW**            | dddd               | 0~511           | Word                           |

<img src="../../drivers/siemens.files/image007.gif" width="595" />

Nota:

d indica il sistema decimale, cifre da 0 a 9;

o indica il sistema ottale, cifre da 0 a 7;

DDD indica il numero di blocco; valori da 0 a 255;

Word nelle note: il registro può essere usato solo come word;

Double word nelle note: nella configurazione il tipo di dato del registro deve essere a 32 bit;

Bit nelle note: il registro può essere usato solo come bit;

Sola lettura nelle note: il registro può essere letto ma non scritto;

I nomi e gli intervalli dei registri supportati possono variare a seconda del modello del dispositivo.

Per i nomi e gli intervalli esatti, consultare la documentazione tecnica del dispositivo collegato

<img src="../../drivers/siemens.files/image008.gif" width="595" />
