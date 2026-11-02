# Controlador Omron

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie SYSMAC C/CPM/CS/CJ. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie SYSMAC C/CPM/CS/CJ</p>
<p>1.  Conexión de hardware</p>
<p>Cable de conexión:</p>
<p>RS232<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span> <span id="OLE_LINK25"></span><span id="OLE_LINK26"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK60"></span><span id="OLE_LINK61"></span><span id="OLE_LINK62"></span><span id="OLE_LINK27"></span><span id="OLE_LINK30"></span><strong>Pantalla táctil COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>SYSMAC CS/CJ</strong></p></td>
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
<td><p>3</p></td>
<td><p>RX</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>9</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/omron.files/image002.gif" width="130" /><img src="../../drivers/omron.files/image003.gif" width="290" /><img src="../../drivers/omron.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC SYSMAC de la serie C/CPM/CS/CJ es DB9M.

**2. Ajustes de software**

Elija OMRON en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC SYSMAC de la serie C/CPM/CS/CJ.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie SYSMAC C/CPM         | Serie SYSMAC C/CPM/CS/CJ                    |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 9600                        | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 7                           | 7/8                                          |
| **Paridad**              | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 2                           | 1/2                                          |
| **Número de estación del PLC**      | 0                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

Serie SYSMAC C/CPM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                                      |
| **IR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Relé de entrada/salida                                                                                          |
| **HR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Relé de retención                                                                                                  |
| **LR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Relé de enlace                                                                                                  |
| **AR_Bit**        | dddd.DD            | 0.0~4095.15     | Bit: Marca auxiliar                                                                                      |
| **T**             | ddd                | 0~255           | Bit: Estado del temporizador                                                                                             |
| **C**             | ddd                | 0~255           | Bit: Estado del contador                                                                                           |
| **IR**            | dddd               | 0~4095          | Palabra: Relé de entrada/salida                                                                                         |
| **HR**            | dddd               | 0~4095          | Palabra: Relé de retención                                                                                                 |
| **LR**            | dddd               | 0~4095          | Palabra: Relé de enlace                                                                                                 |
| **AR**            | dddd               | 0~4095          | Palabra: Marca auxiliar                                                                                     |
| **TC**            | ddd                | 0~255           | Palabra: Valor del temporizador                                                               |
| **DM**            | dddd               | 0~9999          | Palabra: Área de datos común |

Serie SYSMAC CS/CJ

|                   |                    |                 |                                                                                         |
|-------------------|--------------------|-----------------|-----------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                             |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit: Área E/S principal                                        |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit: Área de trabajo                                            |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit: Área de retención                                         |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit: Área auxiliar, solo lectura: 7.168 bits: A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit: Área de datos común                                     |
| **T**             | dddd               | 0~4095          | Bit: Estado del temporizador                                                                    |
| **C**             | dddd               | 0~4095          | Bit: Estado del contador                                                                  |
| **CIO**           | dddd               | 0~3189          | Palabra: Área E/S principal                                                                     |
| **W**             | dddd               | 0~6143          | Palabra: Área de trabajo                                                                         |
| **H**             | dddd               | 0~511           | Palabra: Área de retención                                                                      |
| **A**             | dddd               | 0~959           | Palabra: Área auxiliar, solo lectura: 448 palabras: A000～A447                                    |
| **D**             | dddd               | 0~32767         | Palabra: Área de datos común                                                                  |
| **TV**            | dddd               | 0~4095          | Palabra: Valor actual del temporizador                                                            |
| **CV**            | dddd               | 0~4095          | Palabra: Valor actual del contador                                                          |

CP1L Tcp/Ip       / Fins-udp

|                   |                    |                 |                                                           |
|-------------------|--------------------|-----------------|-----------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                               |
| **CIO_Bit**       | dddd.DD            | 0.0~3189.15     | Bit: Área E/S principal                                        |
| **W_Bit**         | dddd.DD            | 0.0~6143.15     | Bit: Área de trabajo                                            |
| **H_Bit**         | dddd.DD            | 0.0~511.15      | Bit: Área de retención                                         |
| **A_Bit**         | dddd.DD            | 0.0~959.15      | Bit: Área auxiliar, solo lectura: 7.168 bits: A00000～A447.15 |
| **D_Bit**         | dddd.DD            | 0.0~32767.15    | Bit: Área de datos común                                     |
| **T**             | dddd               | 0~4095          | Bit: Estado del temporizador                                      |
| **C**             | dddd               | 0~4095          | Bit: Estado del contador                                    |
| **CIO**           | dddd               | 0~3189          | Palabra: Área E/S principal                                       |
| **W**             | dddd               | 0~6143          | Palabra: Área de trabajo                                           |
| **H**             | dddd               | 0~511           | Palabra: Área de retención                                        |
| **A**             | dddd               | 0~959           | Palabra: Área auxiliar, solo lectura: 448 palabras: A000～A447      |
| **D**             | dddd               | 0~32767         | Palabra: Área de datos común                                    |
| **TV**            | dddd               | 0~4095          | Palabra: Valor actual del temporizador                              |
| **CV**            | dddd               | 0~4095          | Palabra: Valor actual del contador                            |

<img src="../../drivers/omron.files/image010.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

DD: 16 bits; rango de entrada 0-15;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/omron.files/image011.gif" width="595" />

 Conexión TCP/IP del CP1L: ajustes

-&gt; Ethernet integrado -&gt; definir la IP y el puerto. Nota:

se recomienda la comunicación FINS-UDP, que permite conectar varias pantallas táctiles al mismo PLC; antes de la comunicación normal hace falta una conexión de handshake, que requiere cierto tiempo

Conexión FINS-UDP:

Ajustes -&gt; Ethernet integrado -&gt; definir la IP y el puerto

El número de nodo de la configuración FINS-UDP debe coincidir con el número de nodo de los ajustes Ethernet de Omron

<img src="../../drivers/omron.files/image008.jpg" width="500" alt="image009.jpg" />
