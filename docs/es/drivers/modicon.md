# Controlador Modicon

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Modicon NEZA/TWIDO/M218. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Modicon NEZA/TWIDO/M218</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p><span id="OLE_LINK19"></span><span id="OLE_LINK20"></span>Cable de conexión:</p>
<p>RS<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span>485</p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><span id="OLE_LINK30"></span><span id="OLE_LINK27"></span><span id="OLE_LINK62"></span><span id="OLE_LINK61"></span><span id="OLE_LINK60"></span><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Modicon NEZA/TWIDO/M218</strong></p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>2</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>1</p></td>
<td><p>TX+</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>7</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

<img src="../../drivers/modicon.files/image002.gif" width="281" /><img src="../../drivers/modicon.files/image003.gif" width="130" /><img src="../../drivers/modicon.files/image004.gif" width="145" />

El conector del HMI es DB9F y el del PLC Modicon de la serie NEZA/TWIDO/M218 es MD8M.

**2. Ajustes de software**

Elija Modicon Corp. en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Modicon de la serie NEZA/TWIDO/M218.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie NEZA                 | Serie NEZA/TWIDO/M218                       |
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

**3. Registros accesibles y rangos de direcciones**

Serie NEZA

|                   |                    |                 |                                                       |
|-------------------|--------------------|-----------------|-------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                           |
| **%MW**           | ddddd              | 0~65535         | Palabra: Registro de datos de palabra |

Serie TWIDO

|                   |                    |                 |                                                                                    |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                        |
| **%M**            | ddddd              | 0~65535         | Bit: Registro de datos de bit   |
| **%MW**           | ddddd              | 0~65535         | Palabra: Registro de datos de palabra |

Serie M218

|                   |                    |                 |                          |
|-------------------|--------------------|-----------------|--------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**              |
| **%MX**           | ddddd.o            | 0~131071.7      | Bit: Registro de datos de bit   |
| **%MW**           | ddddd              | 0~65535         | Palabra: Registro de datos de palabra |

<img src="../../drivers/modicon.files/image005.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/modicon.files/image006.gif" width="595" />
