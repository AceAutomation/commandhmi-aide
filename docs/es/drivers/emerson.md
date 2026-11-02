# Controlador Emerson

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los <span id="OLE_LINK120"></span><span id="OLE_LINK121"></span>Registros de los PLC de la serie Emerson EC. La comunicación serie se establece entre el puerto serie del HMI y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Emerson EC</p>
<p>1.  Conexión de hardware</p>
<p>Cable de conexión:</p>
<p>RS232</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Emerson EC</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>4</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>3</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/emerson.files/image002.gif" width="146" /><img src="../../drivers/emerson.files/image003.gif" width="281" /><img src="../../drivers/emerson.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC Emerson de la serie EC es MD8M.

**2. Ajustes de software**

Elija Emerson Network Power en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Emerson de la serie EC.

Parámetros de conexión por defecto de la pantalla táctil

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | EC Series (RTU)             | EC Series (RTU)                              |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 7                           | 7/8                                          |
| **Paridad**              | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                             |
|-------------------|--------------------|-----------------|---------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                 |
| X                 | ooo                | 0~377           | Bit: Entrada, solo lectura      |
| Y                 | ooo                | 0~377           | Bit: Salida                |
| M                 | dddd               | 0~7999          | Bit: Relé interno (marca)                         |
| SM                | ddd                | 0~255           | Bit: Relé interno especial                 |
| S                 | ddd                | 0~999           | Bit: Relé de etapa                         |
| T                 | ddd                | 0~255           | Bit: Estado del temporizador                           |
| C                 | ddd                | 0~255           | Bit: Estado del contador                         |
| D                 | dddd               | 0~7999          | Palabra: Memoria de datos temporal                |
| SD                | ddd                | 0~255           | Palabra: Memoria de datos temporal especial        |
| TV                | ddd                | 0~255           | Palabra: Valor actual del temporizador                |
| CV                | ddd                | 0~255           | Palabra: Valor actual del contador              |
| Z                 | dd                 | 0~15            | Palabra: Registro de direccionamiento indexado           |
| D_Double          | dddd               | 0~7999          | Doble palabra: Memoria de datos temporal         |
| CV_Double         | ddd                | 200~255         | Doble palabra: Valor actual del contador       |
| SD_Double         | ddd                | 0~255           | Doble palabra: Memoria de datos temporal especial |

<img src="../../drivers/emerson.files/image005.gif" width="600" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/emerson.files/image006.gif" width="600" />
