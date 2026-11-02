# Controlador Koyo

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Koyo SN. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p> Cómo establecer la conexión con un PLC de la serie Koyo SN</p>
<p><strong>1.</strong> <strong>Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232 (puerto serie, protocolo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p>HMI HM COM1/COM2</p></td>
<td colspan="2"><p>Serie Koyo SN</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>4</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/koyo.files/image006.gif" width="278" /><img src="../../drivers/koyo.files/image007.gif" width="130" /><img src="../../drivers/koyo.files/image008.gif" width="90" />

El conector del HMI es DB9F y el del PLC Koyo de la serie SN es un conector modular de 6 pines.

**2. Ajustes de software**

Elija Koyo Electronics en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Koyo de la serie SN.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie Koyo SN              | Serie Koyo SN                               |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**              | ODD                         | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Serie Koyo SN**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                    |
| **I**             | ooo                | 0~377           | Bit: Relé de entrada, solo lectura    |
| **O**             | ooo                | 0~377           | Bit: Relé de salida              |
| **M**             | oooo               | 0~1177          | Bit: Relé auxiliar (marca)           |
| **SP**            | ooo                | 0~777           | Bit: Relé auxiliar especial   |
| **S**             | ooo                | 0~177           | Bit: Relé de etapa            |
| **T**             | ooo                | 0~177           | Bit: Temporizador                     |
| **C**             | ooo                | 0~177           | Bit: Contador                   |
| **R**             | ooooo              | 0~13777         | Palabra: Registro de datos            |
| **TR**            | ooooo              | 0~13777         | Palabra: Valor actual del temporizador   |
| **CR**            | ooooo              | 0~13777         | Palabra: Valor actual del contador |
| **SR**            | ooooo              | 0~13777         | Palabra: Registro de datos especial    |

**4. Serie Koyo DIRECT**

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                    |
| **X**             | ooo                | 0~3777          | Bit: Relé de entrada, solo lectura    |
| **Y**             | ooo                | 0~3777          | Bit: Relé de salida              |
| **GX**            | oooo               | 0~7777          | Bit: Relé de entrada, solo lectura    |
| **GY**            | oooo               | 0~7777          | Bit: Relé de salida              |
| **C**             | oooo               | 0~7777          | Bit: Contador                   |
| **S**             | oooo               | 0~1777          | Bit: Relé de etapa            |
| **SP**            | oooo               | 0~1777          | Bit: Relé auxiliar especial   |
| **CT**            | ooo                | 0~777           | Bit: Contador                   |
| **T**             | ooo                | 0~777           | Bit: Temporizador                     |
| **V**             | oooo               | 0~77777         | Palabra: Registro de datos especial    |
| **TV**            | ooo                | 0~777           | Palabra: Valor actual del temporizador   |
| **CV**            | ooo                | 0~777           | Palabra: Valor actual del contador |

KV-Nano

|                |              |              |                                            |
|----------------|--------------|--------------|--------------------------------------------|
| **寄存器名称** | **地址格式** | **输入范围** | **备注**                                   |
| **R**          | ddddd        | 0~59915      | Bit: Relé                            |
| **B**          | DDDD         | 0~1FFF       | Bit: Relé de enlace                       |
| **MR**         | ddddd        | 0~59915      | Bit：Marca auxiliar interna         |
| **LR**         | ddddd        | 0~19915      | Bit: Relé de enclavamiento                   |
| **CR**         | dddd         | 0~8915       | Bit: Relé de control                    |
| **VB**         | DDDD         | 0~1FFF       | Bit: Relé de trabajo                       |
| **T**          | ddd          | 0~511        | Bit: Temporizador                            |
| **C**          | ddd          | 0~255        | Bit: Contador                          |
| **DM**         | dddd         | 0~32767      | Palabra：Memoria de datos                         |
| **W**          | DDDD         | 0~3FFF       | Palabra：Registro de enlace                        |
| **TM**         | dddd         | 0~511        | Palabra：Memoria de datos temporal               |
| **Z**          | dddd         | 1~12         | Palabra：Registro de índice                       |
| **TC**         | dddd         | 0~511        | Doble palabra：Temporizador (valor actual)         |
| **TS**         | dddd         | 0~511        | Doble palabra：Temporizador (consigna)         |
| **CC**         | ddd          | 0~255        | Doble palabra：Contador (valor actual)       |
| **CS**         | ddd          | 0~255        | Doble palabra：Contador (consigna)       |
| **CTH**        | d            | 0~3          | Doble palabra：Contador rápido            |
| **CTC**        | d            | 0~7          | Doble palabra：Comparador del contador rápido |
| **CM**         | dddd         | 0~8999       | Palabra：Memoria de control                      |
| **VM**         | dddd         | 0~9999       | Palabra：Memoria de trabajo                       |

<img src="../../drivers/koyo.files/image009.gif" width="595" />

Nota:

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/koyo.files/image010.gif" width="595" />
