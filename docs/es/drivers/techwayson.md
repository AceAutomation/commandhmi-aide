# Controlador Techwayson

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie TaiLing DX. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie TaiLing DX</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232 <span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>(puerto serie, protocolo RS232)</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie TaiLing DX</strong></p></td>
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
<td><p>5</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/techwayson.files/image002.gif" width="130" /><img src="../../drivers/techwayson.files/image003.gif" width="290" /><img src="../../drivers/techwayson.files/image004.gif" width="129" /></p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC es MD8M.

**2. Ajustes de software**

Elija TaiLing Electric en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC TaiLing de la serie DX.

Parámetros de conexión por defecto del HMI HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie Techwayson V80       | Serie Techwayson V80                        |
| **Tipo de puerto** | RS232                       | RS232                                        |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                           | 7/8                                          |
| **Paridad**                  | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 1                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión**  | Sí                         |
| **Simulación en línea**   | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                              |
|-------------------|--------------------|-----------------|----------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                  |
| **X**             | oooo               | 0 a 377        | Bit: Bobina de entrada, solo lectura                   |
| **Y**             | oooo               | 0 a 377        | Bit: Bobina de salida                             |
| **M**             | dddd               | 0 a 7999       | Bit: Relé intermedio (marca)                      |
| **SM**            | dddd               | 8000 a 8999    | Bit: Relé intermedio especial              |
| **S**             | dddd               | 0 a 999        | Bit: Bit de estado                               |
| **T**             | dddd               | 0 a 256        | Bit: Estado del temporizador                             |
| **C**             | dddd               | 0 a 256        | Bit: Estado del contador                           |
| **D**             | dddd               | 0 a 7999       | Palabra: Registro                               |
| **SD**            | dddd               | 8000 a 8999    | Palabra: Registro especial                       |
| **TV**            | dddd               | 0 a 255        | Palabra: Valor actual del temporizador             |
| **CV**            | dddd               | 0 a 199        | Palabra: Valor actual del contador           |
| **CV32**          | dddd               | 200 a 255      | Doble palabra: Valor actual del contador de 32 bits |

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                            |
| **0x**            | dddd               | 1~9984          | Bit: Bobina de salida                       |
| **1x**            | dddd               | 1~2048          | Bit: Bobina de entrada, solo lectura             |
| **3x**            | dddd               | 1~512           | Palabra: Registro de entrada de 16 bits, solo lectura |
| **4x**            | dddd               | 1~9999          | Palabra: Registro de retención de 16 bits          |

<img src="../../drivers/techwayson.files/image005.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/techwayson.files/image006.gif" width="595" />
