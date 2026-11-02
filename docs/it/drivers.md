# Driver dei dispositivi

Questo capitolo descrive i dispositivi compatibili con gli HMI serie HM di ACE AUTOMATION.

L'impostazione dei driver di I/O dei dispositivi è fondamentale per la configurazione. Gli HMI serie HM possono comunicare con PLC, microcontrollori, inverter e altri dispositivi industriali, tra cui la grande maggioranza dei PLC: CommandHMI, MITSUBISHI, OMRON, SIEMENS, ALLEN-BRADLEY Rockwell, MATSUSHITA, DELTA, FATEK, ecc. Possono inoltre monitorare e controllare dispositivi industriali tramite protocolli specifici, come MODBUS RTU / ASCII, HOSTLINK e alcuni protocolli personalizzati.

Il driver di I/O di ogni PLC o dispositivo è contenuto in un file: nella creazione di un progetto basta selezionare il PLC o il dispositivo corrispondente, senza altre operazioni di programmazione complesse. CommandHMI, il software di configurazione degli HMI serie HM, permette di accedere a tutti i tipi di registri e relè della maggior parte dei PLC e dispositivi con operazioni di configurazione semplici. Sono disponibili tre modalità operative: sola lettura, sola scrittura, lettura e scrittura, per soddisfare le diverse esigenze del controllo industriale.

Per facilitare il collegamento a dispositivi diversi, il fornitore offre un servizio di sviluppo di driver su richiesta: basta fornire la documentazione del protocollo di comunicazione del dispositivo. Per informazioni, contattare il fornitore ai recapiti indicati alla fine del manuale.

PLC supportati dagli HMI serie HM:

|                                                         |                                                |                                     |                                          |
|---------------------------------------------------------|------------------------------------------------|-------------------------------------|------------------------------------------|
| **Produttore (marca)** | **Modello** | **Protocollo di comunicazione** | **Tipo di collegamento** |
| [AIBUS](drivers/aibus.md) | Serie AI | Protocollo AIBUS | Collegamento diretto (porta seriale) |
| [Allen-Bradley](drivers/allen-bradley.md) | Serie MicroLogix | Protocollo DF1 | Collegamento diretto (porta seriale) |
| [Can_communication](drivers/can_communication.md) | Can | Can | Collegamento diretto (porta seriale) |
| [Delta Corporation](drivers/delta.md) | Serie DVP | Protocollo proprietario Delta | Collegamento diretto (porta seriale) |
| [Emerson Network Power](drivers/emerson.md) | Serie EC | Protocollo proprietario Emerson | Collegamento diretto (porta seriale) |
| [Fatek Automation Corporation](drivers/fatek.md) | Serie FB | Protocollo proprietario Fatek | Collegamento diretto (porta seriale) |
| [Fuji Electric Corporation](drivers/fuji.md) | Serie NB | Protocollo proprietario Fuji | Collegamento diretto (porta seriale) |
| [GE Corporation](drivers/ge.md) | GE SNP-X/CCM | Protocollo proprietario GE | Collegamento diretto (porta seriale) |
| [Haiwell Technology Corporation](drivers/haiwell.md) | Serie E/S/H | Protocollo proprietario Haiwell | Collegamento diretto (porta seriale) |
| [Hitachi Industrial](drivers/hitachi.md) | Serie E/EH | Protocollo proprietario Hitachi | Collegamento diretto (porta seriale) |
| [HollySys Group](drivers/hollysys.md) | Serie LM | Protocollo proprietario HollySys | Collegamento diretto (porta seriale) |
| [IDEC Corporation](drivers/idec.md) | Serie FC4A/FC5A | Protocollo proprietario IDEC | Collegamento diretto (porta seriale) |
| [Inovance Technology Corporation](drivers/inovance.md) | Serie H1u/H2u | Protocollo proprietario Inovance | Collegamento diretto (porta seriale) |
| [Invt](drivers/invt.md) | IVC1,IVC1L,IVCIS,IVC2L,IVC3 | Protocollo proprietario Invt | Collegamento diretto (porta seriale) |
| [Keyence Corporation](drivers/keyence.md) | KV-1000/700 KV-L20(R), KV-/40 KV-P16 | Protocollo proprietario Keyence | Collegamento diretto (porta seriale) |
| [Koyo Electronics](drivers/koyo.md) | Serie SN | Protocollo proprietario Koyo | Collegamento diretto (porta seriale) |
| [LG Industrial Systems](drivers/lg.md) | Serie Master-K | Protocollo proprietario LG | Collegamento diretto (porta seriale) |
| [Matsushita](drivers/matsushita.md) | Serie FP | Protocollo proprietario Matsushita | Collegamento diretto (porta seriale) |
| [Mitsubishi](drivers/mitsubishi.md) | Melsec-FX/FX2N/FX3U/FX3G, serie Melsec-Q_C24N | Protocollo proprietario Mitsubishi | Collegamento diretto (porta seriale) |
| [Modbus](drivers/modbus.md) | Dispositivi RTU/ASCII, dispositivi RTU TCP/IP | Protocollo Modbus | Collegamento diretto (porta seriale/Ethernet) |
| [Modicon Corporation](drivers/modicon.md) | Serie NEZA/TWIDO/M218 | Protocollo Modbus | Collegamento diretto (porta seriale) |
| [Nanda Auto Technology](drivers/nanda.md) | Serie NA-200/NA-400 | Protocollo proprietario Nanda Auto | Collegamento diretto (porta seriale) |
| [Omron](drivers/omron.md) | Serie C/CPM, serie CS/CJ | Protocollo proprietario Omron | Collegamento diretto (porta seriale) |
|                                                         |                                                |                                     |                                          |
| [Siemens](drivers/siemens.md) | S7-200(PPI), S7-300(MPI), S7-1200 | Protocollo proprietario Siemens | Collegamento diretto (porta seriale) |
| [TaiAn Technology](drivers/taian.md) | Serie TP03 | Protocollo proprietario TaiAn | Collegamento diretto (porta seriale) |
| [TaiLing Electric](drivers/tailing.md) | Serie DX | Protocollo proprietario TaiLing | Collegamento diretto (porta seriale) |
| [Techwayson Technology](drivers/techwayson.md) | Serie V | Protocollo proprietario Techwayson | Collegamento diretto (porta seriale) |
| [Vigor Electric Corporation](drivers/vigor.md) | Serie V/VH/VB/M | Protocollo proprietario Vigor | Collegamento diretto (porta seriale) |
| [Xinje Electronic](drivers/xinje.md) | Serie XC/XCM | Protocollo proprietario XinJe | Collegamento diretto (porta seriale) |
| [Yokogawa Electric Corporation](drivers/yokogawa.md) | Serie FA-M3 | Protocollo proprietario Yokogawa | Collegamento diretto (porta seriale) |
| [ZhengHang Electronics](drivers/zhenghang.md) | Serie A4/A5 | Protocollo proprietario ZhengHang | Collegamento diretto (porta seriale) |

• Piedinatura delle porte COM1/COM2 degli HMI serie HM

Gli HMI serie HM hanno un connettore maschio a nove pin, quindi il cavo di collegamento deve avere un connettore femmina a nove pin. La piedinatura è la seguente:

|                             |     |
|-----------------------------|-----|
| **HMI serie HM COM1/COM2** |     |
| **1**                       |     |
| **2**                       | RX  |
| **3**                       | TX  |
| **4**                       | KZ  |
| **5**                       | GND |
| **6**                       | RX- |
| **7**                       | RX+ |
| **8**                       |     |
| **9**                       |     |

• RX: ricezione RS232

•  TX: trasmissione RS232

• KZ: porta di controllo

• GND: massa

• RX-: ricezione RS422 -

• RX+: ricezione RS422 +

• TX-: trasmissione RS422 - / RS485 B

• TX+: trasmissione RS422 + / RS485 A

<img src="../drivers.files/image002.gif" width="761" />

Nota

·Pin 2/3/5 per la comunicazione RS232;

·Pin 6/7/8/9 per la comunicazione RS422;

·Pin 8/9 per la comunicazione RS485.

<img src="../drivers.files/image003.gif" width="761" />
