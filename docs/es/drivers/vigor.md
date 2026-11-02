# Controlador Vigor

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Vigor V/VH/VB/M. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Vigor V/VH/VB/M</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Vigor V/VH/VB/M</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>3</p></td>
<td><p>TX</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>2</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>4</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/vigor.files/image002.gif" width="63" /><img src="../../drivers/vigor.files/image003.gif" width="318" /><img src="../../drivers/vigor.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC Vigor de la serie V/VH/VB/M es DB9M.

**2. Ajustes de software**

Elija Vigor Electric Corp. en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Vigor de la serie V/VH/VB/M.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie V/VH/VB/M            | Serie V/VH/VB/M                             |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 7                           | 7/8                                          |
| **Paridad**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 0                           | 0 a 255                                     |
| **Número de estación del HMI**      | 0                           | 0 a 255                                     |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión**  | Sí                         |
| **Simulación en línea**   | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                       |
|-------------------|--------------------|-----------------|---------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                           |
| **X**             | ooo                | 0 a 777        | Bit: Contacto de entrada                    |
| **Y**             | ooo                | 0 a 777        | Bit: Contacto de salida                   |
| **M**             | dddd               | 0 a 8999       | Bit: Relé interno (marca)                   |
| **SM**            | dddd               | 9000 a 9255    | Bit: Relé interno especial           |
| **S**             | dddd               | 0 a 999        | Bit: Relé de etapa                   |
| **T**             | ddd                | 0 a 255        | Bit: Estado del temporizador                      |
| **C**             | ddd                | 0 a 255        | Bit: Estado del contador                    |
| **D**             | dddd               | 0 a 8999       | Palabra: Registro de datos                   |
| **SD**            | dddd               | 9000 a 9255    | Palabra: Registro de datos especial           |
| **TV**            | ddd                | 0 a 255        | Palabra: Valor actual del temporizador      |
| **CV**            | ddd                | 0 a 199        | Palabra: Valor actual del contador    |
| **CV32**          | ddd                | 200 a 255      | Palabra: Valor actual del contador de 32 bits |

<img src="../../drivers/vigor.files/image005.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo;

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/vigor.files/image005.gif" width="595" />
