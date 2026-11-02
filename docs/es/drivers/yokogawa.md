# Controlador Yokogawa

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC Yokogawa de la serie FA-M3. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

Cómo establecer la conexión con un PLC Yokogawa de la serie FA-M3

**1. Conexión de hardware**

Cable de conexión:

RS232 <span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<tbody>
<tr class="odd">
<td colspan="2"><p>Serie HM COM1/COM2</p></td>
<td colspan="3"><p><strong>Serie Yokogawa FA-M3</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>5</strong></p></td>
<td><p>GND</p></td>
<td><p>5</p></td>
<td><p>SG</p></td>
<td rowspan="2"><p>4-5 puenteados</p>
<p>Resistencia de 220 Ω en serie</p></td>
</tr>
<tr class="odd">
<td><p><strong>6</strong></p></td>
<td><p>RX-</p></td>
<td><p>4</p></td>
<td><p>SDB</p></td>
</tr>
<tr class="even">
<td><p><strong>7</strong></p></td>
<td><p>RX+</p></td>
<td><p>3</p></td>
<td><p>SDA</p></td>
<td rowspan="2"><p>2-3 puenteados</p>
<p>Resistencia de 220 Ω en serie</p></td>
</tr>
<tr class="odd">
<td><p><strong>8</strong></p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>RDB</p></td>
</tr>
<tr class="even">
<td><p><strong>9</strong></p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td colspan="2"><p>RDA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>6</p></td>
<td><p>CSA</p></td>
<td rowspan="2"><p>6-7 puenteados</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>7</p></td>
<td><p>ERA</p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td><p>8</p></td>
<td><p>CSB</p></td>
<td rowspan="2"><p>8-9 puenteados</p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
<td><p>9</p></td>
<td><p>ERB</p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC Yokogawa de la serie FA-M3 es SIO.

**2. Ajustes de software**

Elija Yokogawa Electric Corp. en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Yokogawa de la serie FA-M3.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Yokogawa FA-M3              | Yokogawa FA-M3                               |
| **Tipo de puerto** | RS422                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0 a 255                                     |
| **Número de estación del HMI**      | 0                           | 0 a 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión**  | Sí                         |
| **Simulación en línea**   | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                               |
| **X**             | ddddd              | 0 a 71664      | Bit: Entrada, no continua, según el número de slot  |
| **Y**             | ddddd              | 0 a 71664      | Bit: Salida, no continua, según el número de slot |
| **M**             | ddddd              | 0 a 16384      | Bit: Relé especial                                        |
| **I**             | ddddd              | 0 a 71024      | Bit: Relé interno (marca)                                       |
| **L**             | ddddd              | 0 a 9984       | Bit: Relé de enlace, no continuo                            |
| **D**             | ddddd              | 0 a 8192       | Palabra: Registro de datos                                       |
| **B**             | ddddd              | 0 a 32768      | Palabra: Registro de archivo                                       |
| **V**             | ddddd              | 0 a 64         | Palabra: Salida digital externa                     |
| **W**             | ddddd              | 0 a 71024      | Palabra: Registro de enlace, no continuo                        |
| **Z**             | ddddd              | 0 a 512        | Palabra: Registro especial                                    |

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/yokogawa.files/image002.gif" width="595" />
