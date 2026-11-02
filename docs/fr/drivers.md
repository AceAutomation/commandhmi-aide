# Pilotes d'équipements

Ce chapitre présente les équipements compatibles avec les IHM de la série HM d'ACE AUTOMATION.

Le réglage des E/S du pilote d'équipement est important pour la configuration. Les IHM de la série HM communiquent avec des automates, microcontrôleurs, variateurs et autres équipements industriels, dont la grande majorité des automates : CommandHMI, MITSUBISHI, OMRON, SIEMENS, ALLEN-BRADLEY Rockwell, MATSUSHITA, DELTA, FATEK, etc. Elles peuvent aussi surveiller et commander certains équipements via des protocoles spécifiques, comme MODBUS RTU / ASCII, HOSTLINK et d'autres protocoles personnalisés.

Le pilote d'E/S de chaque automate ou équipement est un fichier : il suffit de choisir l'automate ou l'équipement correspondant lors de la création du projet, sans autre programmation complexe. CommandHMI, logiciel de configuration des IHM de la série HM, donne accès aux registres et relais de la plupart des automates et équipements par une configuration simple. Trois modes sont disponibles : lecture seule, écriture seule, lecture et écriture, pour répondre aux besoins du contrôle industriel.

Pour faciliter la connexion à d'autres équipements, le fabricant propose de développer des pilotes à la demande : il suffit de fournir la documentation du protocole de communication de l'équipement. Les coordonnées de contact figurent à la fin de ce manuel.

Automates pris en charge par les IHM de la série HM :

|                                                         |                                                |                                     |                                          |
|---------------------------------------------------------|------------------------------------------------|-------------------------------------|------------------------------------------|
| **Fabricant (marque)**                                  | **Modèle**                                     | **Protocole de communication**      | **Mode de connexion**                    |
| [AIBUS](drivers/aibus.md)                               | Série AI                                       | Protocole AIBUS                     | Connexion directe (port série)           |
| [Allen-Bradley](drivers/allen-bradley.md)               | Série MicroLogix                               | Protocole DF1                       | Connexion directe (port série)           |
| [Can_communication](drivers/can_communication.md)       | Can                                            | Can                                 | Connexion directe (port série)           |
| [Delta Corporation](drivers/delta.md)                   | Série DVP                                      | Protocole propriétaire Delta        | Connexion directe (port série)           |
| [Emerson Network Power](drivers/emerson.md)             | Série EC                                       | Protocole propriétaire Emerson      | Connexion directe (port série)           |
| [Fatek Automation Corporation](drivers/fatek.md)        | Série FB                                       | Protocole propriétaire Fatek        | Connexion directe (port série)           |
| [Fuji Electric Corporation](drivers/fuji.md)            | Série NB                                       | Protocole propriétaire Fuji         | Connexion directe (port série)           |
| [GE Corporation](drivers/ge.md)                         | GE SNP-X/CCM                                   | Protocole propriétaire GE           | Connexion directe (port série)           |
| [Haiwell Technology Corporation](drivers/haiwell.md)    | Séries E/S/H                                   | Protocole propriétaire Haiwell      | Connexion directe (port série)           |
| [Hitachi Industrial](drivers/hitachi.md)                | Séries E/EH                                    | Protocole propriétaire Hitachi      | Connexion directe (port série)           |
| [HollySys Group](drivers/hollysys.md)                   | Série LM                                       | Protocole propriétaire HollySys     | Connexion directe (port série)           |
| [IDEC Corporation](drivers/idec.md)                     | Séries FC4A/FC5A                               | Protocole propriétaire IDEC         | Connexion directe (port série)           |
| [Inovance Technology Corporation](drivers/inovance.md)  | Séries H1u/H2u                                 | Protocole propriétaire Inovance     | Connexion directe (port série)           |
| [Invt](drivers/invt.md)                                 | IVC1,IVC1L,IVCIS,IVC2L,IVC3                    | Protocole propriétaire Invt         | Connexion directe (port série)           |
| [Keyence Corporation](drivers/keyence.md)               | KV-1000/700 KV-L20(R), KV-/40 KV-P16           | Protocole propriétaire Keyence      | Connexion directe (port série)           |
| [Koyo Electronics](drivers/koyo.md)                     | Série SN                                       | Protocole propriétaire KoYo         | Connexion directe (port série)           |
| [LG Industrial Systems](drivers/lg.md)                  | Série Master-K                                 | Protocole propriétaire LG           | Connexion directe (port série)           |
| [Matsushita](drivers/matsushita.md)                     | Série FP                                       | Protocole propriétaire Matsushita   | Connexion directe (port série)           |
| [Mitsubishi](drivers/mitsubishi.md)                     | Melsec-FX/FX2N/FX3U/FX3G，série Melsec-Q_C24N  | Protocole propriétaire Mitsubishi   | Connexion directe (port série)           |
| [Modbus](drivers/modbus.md)                             | Équipements RTU/ASCII，équipements RTU TCP/IP   | Protocole Modbus                    | Connexion directe (port série/Ethernet)  |
| [Modicon Corporation](drivers/modicon.md)               | Séries NEZA/TWIDO/M218                         | Protocole Modbus                    | Connexion directe (port série)           |
| [Nanda Auto Technology](drivers/nanda.md)               | Séries NA-200/NA-400                           | Protocole propriétaire Nanda Auto   | Connexion directe (port série)           |
| [Omron](drivers/omron.md)                               | Séries C/CPM，séries CS/CJ                     | Protocole propriétaire Omron        | Connexion directe (port série)           |
|                                                         |                                                |                                     |                                          |
| [Siemens](drivers/siemens.md)                           | S7-200(PPI)，S7-300(MPI), S7-1200              | Protocole propriétaire Siemens      | Connexion directe (port série)           |
| [TaiAn Technology](drivers/taian.md)                    | Série TP03                                     | Protocole propriétaire TaiAn        | Connexion directe (port série)           |
| [TaiLing Electric](drivers/tailing.md)                  | Série DX                                       | Protocole propriétaire TaiLing      | Connexion directe (port série)           |
| [Techwayson Technology](drivers/techwayson.md)          | Série V                                        | Protocole propriétaire Techwayson   | Connexion directe (port série)           |
| [Vigor Electric Corporation](drivers/vigor.md)          | Séries V/VH/VB/M                               | Protocole propriétaire Vigor        | Connexion directe (port série)           |
| [Xinje Electronic](drivers/xinje.md)                    | Séries XC/XCM                                  | Protocole propriétaire XinJe        | Connexion directe (port série)           |
| [Yokogawa Electric Corporation](drivers/yokogawa.md)    | Série FA-M3                                    | Protocole propriétaire Yokogawa     | Connexion directe (port série)           |
| [ZhengHang Electronics](drivers/zhenghang.md)           | Séries A4/A5                                   | Protocole propriétaire ZhengHang    | Connexion directe (port série)           |

• Brochage des ports COM1/COM2 des IHM de la série HM

Les IHM de la série HM utilisent un connecteur mâle 9 broches ; le câble de liaison doit donc avoir une prise femelle 9 broches. Le brochage est le suivant :

|                             |     |
|-----------------------------|-----|
| **IHM série HM COM1/COM2** |     |
| **1**                       |     |
| **2**                       | RX  |
| **3**                       | TX  |
| **4**                       | KZ  |
| **5**                       | GND |
| **6**                       | RX- |
| **7**                       | RX+ |
| **8**                       |     |
| **9**                       |     |

• RX : réception RS232

•  TX : émission RS232

• KZ : port de contrôle

• GND : masse

• RX- : réception RS422 -

• RX+ : réception RS422 +

• TX- : émission RS422 - / RS485 B

• TX+ : émission RS422 + / RS485 A

<img src="../drivers.files/image002.gif" width="761" />

Remarque

· Broches 2/3/5 pour la communication RS232 ;

· Broches 6/7/8/9 pour la communication RS422 ;

· Broches 8/9 pour la communication RS485.

<img src="../drivers.files/image003.gif" width="761" />
