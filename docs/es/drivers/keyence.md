# Controlador Keyence

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Keyence KV/VisualKV. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Keyence KV/VisualKV</p>
<p><strong>1. Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232 (puerto serie, protocolo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Keyence KV/VisualKV</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>2</p></td>
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
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/keyence.files/image002.gif" width="130" /><img src="../../drivers/keyence.files/image003.gif" width="90" /><img src="../../drivers/keyence.files/image004.gif" width="278" />

El conector del HMI es DB9F y el del PLC Keyence de la serie KV/VisualKV es un conector modular de 6 pines.

**2. Ajustes de software**

Elija Keyence Corporation en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Keyence de la serie KV/VisualKV.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | KV-1000/700 KV-L20(R)       | KV-1000/700 KV-L20(R)/ KV-/40 KV-P16         |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 0                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

l  KV-1000/700 KV-L20(R)

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                    |
| **R**             | dddDD              | 0~99915         | Bit: Relé de entrada/salida        |
| **MR**            | dddDD              | 0~3915          | Bit: Marca auxiliar interna  |
| **LR**            | dddDD              | 0~3999          | Bit: Relé de enclavamiento            |
| **CR**            | ddDD               | 0~3999          | Bit: Relé de control             |
| **T**             | dddd               | 0~65534         | Bit: Temporizador                     |
| **C**             | dddd               | 0~65534         | Bit: Contador                   |
| **DM**            | ddddd              | 0~32766         | Palabra: Memoria de datos             |
| **EM**            | ddddd              | 0~511           | Palabra: Memoria de datos extendida    |
| **FM**            | ddddd              | 0~11998         | Palabra: Registro de archivo            |
| **TM**            | ddd                | 0~3999          | Palabra: Memoria de datos temporal   |
| **CM**            | ddddd              | 0~3999          | Palabra: Memoria de control          |
| **TV**            | dddd               | 0~99915         | Palabra: Valor actual del temporizador   |
| **CV**            | dddd               | 0~3915          | Palabra: Valor actual del contador |

l  KV-10/16/24/40 KV-P16

|                   |                    |                 |                                           |
|-------------------|--------------------|-----------------|-------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                               |
| RLY               | dddDD              | 0~99915         | Bit: Relé                                |
| T                 | dddd               | 0~999           | Bit: Temporizador                                |
| C                 | dddd               | 0~999           | Bit: Contador                              |
| DM                | ddddd              | 0~9999          | Palabra: Memoria de datos                        |
| TM                | ddd                | 0~99            | Palabra: Memoria de datos temporal              |
| TV_c              | dddd               | 0~999           | Palabra: Valor actual del temporizador              |
| TV_p              | dddd               | 0~999           | Palabra: Valor preseleccionado del temporizador               |
| CV_c              | dddd               | 0~999           | Palabra: Valor actual del contador            |
| CV_p              | dddd               | 0~999           | Palabra: Valor preseleccionado del contador             |
| CTH               | dddd               | 0~9             | Palabra: Valor actual del contador rápido |

l  KV-Nano

|                   |                    |                 |                                      |
|-------------------|--------------------|-----------------|--------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                          |
| **R**             | ddddd              | 0~59915         | Bit: Relé                      |
| **B**             | DDDD               | 0~1FFF          | Relé de enlace                           |
| **MR**            | ddddd              | 0~59915         | Marca auxiliar interna             |
| **LR**            | ddddd              | 0~19915         | Relé de enclavamiento                       |
| **CR**            | dddd               | 0~8915          | Relé de control                        |
| **VB**            | DDDD               | 0~1FFF          | Relé de trabajo                        |
| **T**             | ddd                | 0~511           | Bit: temporizador                            |
| **C**             | ddd                | 0~255           | Bit: Contador                         |
| **DM**            | dddd               | 0~32767         | Memoria de datos                          |
| **W**             | DDDD               | 0~3FFF          | Registro de enlace                        |
| **TM**            | dddd               | 0~511           | Memoria de datos temporal               |
| **Z**             | dddd               | 1~12            | Registro de índice                       |
| **TC**            | dddd               | 0~511           | Doble palabra: Temporizador (valor actual)   |
| **TS**            | dddd               | 0~511           | Doble palabra: Temporizador (consigna)       |
| **CC**            | ddd                | 0~255           | Doble palabra: Contador (valor actual) |
| **CS**            | ddd                | 0~255           | Doble palabra: Contador (consigna)     |
| **CTH**           | d                  | 0~3             | Contador rápido                   |
| **CTC**           | d                  | 0~7             | Doble palabra: Comparador rápido   |
| **CM**            | dddd               | 0~8999          | Memoria de control                       |
| **VM**            | dddd               | 0~9999          | Memoria de trabajo                       |

<img src="../../drivers/keyence.files/image005.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

DD: 16 bits, rango de entrada 0-15;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/keyence.files/image005.gif" width="595" />
