# Controlador Allen-Bradley

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de dispositivos AIBUS mediante el protocolo AIBUS. La comunicación serie se establece entre el puerto serie del HMI y el del dispositivo AIBUS. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del dispositivo AIBUS.

**Cómo establecer la conexión con el equipo**

**1. Conexión de hardware**

Cable de conexión:

RS232 (puerto serie, protocolo RS232)

|                             |     |                   |     |
|-----------------------------|-----|-------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Dispositivo AIBUS**  |     |
| 2                           | RX  | Pin definido por el usuario | TX  |
| 3                           | TX  | Pin definido por el usuario | RX  |
| 5                           | GND | Pin definido por el usuario | GND |

<img src="../../drivers/allen-bradley.files/image002.gif" width="130" /><img src="../../drivers/allen-bradley.files/image003.gif" width="280" /><img src="../../drivers/allen-bradley.files/image004.gif" width="145" />

ControlLogix/CompactLogix:

|                             |     |                         |     |
|-----------------------------|-----|-------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Allen-Bradley（AB）** |     |
| 2                           | RX  | 3                       | TX  |
| 3                           | TX  | 2                       | RX  |
| 5                           | GND | 5                       | GND |

<img src="../../drivers/allen-bradley.files/image005.gif" width="129" /><img src="../../drivers/allen-bradley.files/image006.gif" width="290" /><img src="../../drivers/allen-bradley.files/image007.gif" width="130" />

El puerto del HMI de la serie HM es DB9F y el del equipo AB es MD8M.

**2. Ajustes de software**

ü Elija Allen-Bradley en el servicio de equipo de la conexión.

ü Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

ü Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

ü Para la configuración del PLC conectado, consulte la documentación técnica del PLC Allen-Bradley.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | MicroLogix DF1_CRC          | MicroLogix DF1_CRC/MicroLogix DF1_BCC        |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | NONE                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 1~31                                         |
| **Número de estación del HMI**      | 0                           | 0~255                                        |
| **Control**                   | CRC                         | BCC                                          |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

Serie SLC/MicroLogix:

|                   |                    |                        |                                |
|-------------------|--------------------|------------------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada**        | **Observaciones**                    |
| **I**             | 1:ddd/o            | 1:0/0~1:255/15         | Bit: Imagen de entradas     |
| **O**             | 0:ddd/o            | 0:0/0~0:255/15         | Bit: Imagen de salidas    |
| **B**             | ddd:ddd/o          | 3:0/0~255:255/15       | Bit: Memoria de bits (marcas)                |
| **S_Bit**         | 2:ddd/o            | 2:0/0~2:255/15         | Bit: bit de estado del sistema          |
| **N_Bit**         | ddd:ddd/o          | 7:0、10:0/0~255:255/15 | Bit: bit de una palabra del registro de datos |
| **S**             | 2:ddd              | 2:0~2:255              | Palabra: palabra de estado del sistema        |
| **ST**            | ddd:ddd.dd         | 0:0.0~255:255.40       | Palabra: palabra de estado del sistema        |
| **N**             | ddd:ddd            | 7:0、10:0~255:255      | Palabra: Registro de datos            |
| **F**             | ddd:ddd            | 8:0~255:255            | Palabra: registro de coma flotante |
| **T_ACC**         | ddd:ddd            | 4:0~255:255            | Palabra: valor ACC del temporizador          |
| **T_PRE**         | ddd:ddd            | 4:0~255:255            | Palabra: valor PRE del temporizador          |
| **C_ACC**         | ddd:ddd            | 5:0~255:255            | Palabra: valor ACC del contador        |
| **C_PRE**         | ddd:ddd            | 5:0~255:255            | Palabra: valor PRE del contador        |

ControlLogix/CompactLogix:

|                   |                    |                  |                                |
|-------------------|--------------------|------------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada**  | **Observaciones**                    |
| **B-Bit**         | ddd:ddd/dd         | 3~225:0~255/0~15 | Bit: bit de una palabra del registro de datos |
| **N_Bit**         | ddd:ddd/dd         | 7~225:0~255/0~15 | Bit: bit de una palabra del registro de datos |
| **N_Bit**         | ddd:ddd/o          | 7:0/0~255:255/7  | Bit: bit de una palabra del registro de datos |
| **S**             | 2:ddd              | 2:0~2:255        | Palabra: palabra de estado del sistema        |
| **N**             | ddd:ddd            | 7:0~255:255      | Palabra: Registro de datos            |
| **F**             | ddd:ddd            | 8:0~255:255      | Palabra: registro de coma flotante |

CompactLogix_L16ER_TCP (puerto: 44818)

|               |                    |                 |                                        |
|---------------|--------------------|-----------------|----------------------------------------|
| Nombre del registro | **Formato de dirección** | **Rango de entrada** | **Observaciones**                            |
| **B**         | ddd.ddd            | 0.0~255.255     | Bit: dirección de tipo bool                 |
| **I**         | Ddd.ddd            | 0.0~255.255     | Palabra: registro entero de 16 bits              |
| **F**         | ddd.ddd            | 0.0~255.99      | Doble palabra: registro de coma flotante de 32 bits |

MicroLogix DF1_TCP            (puerto: 44818)

|               |                    |                  |                                                    |
|---------------|--------------------|------------------|----------------------------------------------------|
| Nombre del registro | **Formato de dirección** | **Rango de entrada**  | **Observaciones**                                        |
| **I**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: imagen de entradas, solo lectura             |
| **O**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: Imagen de salidas                         |
| **B**         | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: memoria de bits                                   |
| **T**         | ddd.ddd            | 0.0~255.255      | Bit: Estado del temporizador                                   |
| **C**         | ddd.ddd            | 0.0~255.255      | Bit: Estado del contador                                 |
| **S_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bit: bit del registro del sistema                |
| **N_Bit**     | ddd.ddd/dd         | 0.0/0~255.255/15 | Bits: bits de un registro de datos                      |
| **S**         | ddd.ddd            | 0.0~255.255      | Palabra: Registro del sistema                              |
| **N**         | ddd.ddd            | 0.0~255.255      | Palabra: registro entero de 16 bits                      |
| **F**         | ddd.ddd            | 0.0~255.255      | Doble palabra: registro de coma flotante de 32 bits |
| **TV**        | ddd.ddd            | 0.0~255.255      | Palabra: Valor actual del temporizador                       |
| **CV**        | ddd.ddd            | 0.0~255.255      | Palabra: Valor actual del contador                        |
| **TS**        | ddd.ddd            | 0.0~255.255      | Palabra: consigna del temporizador                          |
| **CS**        | ddd.ddd            | 0.0~255.255      | Palabra: consigna del contador                            |

**4. Conexión de los HMI de la serie HM con los PLC ControlLogix y CompactLogix de Allen-Bradley**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p>Abra RSLinx y configure el controlador de comunicación del PLC</p>
<p><img src="../../drivers/allen-bradley.files/image008.gif" width="349" /></p>
<p>Cree un controlador; elija conexión por puerto serie y dispositivos RS-232 DF1</p>
<p><img src="../../drivers/allen-bradley.files/image009.gif" width="425" /></p>
<p>Si hay un cable entre el PC y el PLC, el PLC aparece en RSLinx tras la configuración</p>
<p><img src="../../drivers/allen-bradley.files/image010.gif" width="430" /></p>
<p>Abra el software de programación RSLogix 5000 y cree su proyecto y nuevos tags</p>
<p><img src="../../drivers/allen-bradley.files/image011.gif" width="282" /></p>
<p>Cree los tags B003, N007 y F008</p>
<p><img src="../../drivers/allen-bradley.files/image012.gif" width="390" /></p>
<p>Lista de tags tras la creación:</p>
<p><img src="../../drivers/allen-bradley.files/image013.gif" width="633" /></p>
<p>Cree la <a href="javascript:;">asignación de direcciones</a></p>
<p><img src="../../drivers/allen-bradley.files/image014.gif" width="428" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image015.gif" width="410" /><strong></strong></p>
<p><strong>Configure los parámetros del PLC</strong></p>
<p><img src="../../drivers/allen-bradley.files/image016.gif" width="807" /><strong></strong></p>
<p><img src="../../drivers/allen-bradley.files/image017.gif" width="552" /><strong></strong></p>
<p>·d: decimal, rango de entrada 0-9;</p>
<p>·o: octal, rango de entrada 0-7;</p>
<p>·Bit en las observaciones: el registro solo puede usarse como bit;</p>
<p>·Palabra en las observaciones: el registro solo puede usarse como palabra;</p>
<p>·Solo lectura en las observaciones: el registro puede leerse pero no escribirse;</p>
<p>·Los nombres y rangos de los registros pueden variar según el modelo de equipo.</p>
<p>Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado </p></td>
</tr>
</tbody>
</table>

Conexión de un PLC CompactLogix de la serie 1769

Nuevas etiquetas de dirección en el PLC

Correspondencia de etiquetas de dirección

Registro        tipo de etiqueta     tamaño del array

B                          bool             255

I                           int                 255

F                          real               100

El formato de etiqueta debe tener 3 caracteres, como B003, I004 y F005

<img src="../../drivers/allen-bradley.files/image018.jpg" width="314" alt="ab_guanli.jpg" />

<img src="../../drivers/allen-bradley.files/image019.jpg" width="390" alt="ab_guanli2.jpg" />

Conexión de un MicroLogix DF1_TCP de la serie 1766

Salvo los registros de E/S, cuyo tamaño no puede definirse, el tamaño del array de los demás registros es 256. El primer número del formato de dirección es el número de archivo. Por ejemplo, el número de archivo de F8 es 8, el de I1 es 1, etc.
