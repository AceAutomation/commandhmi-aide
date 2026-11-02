# Controlador Hitachi

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC Hitachi de la serie E/EH. La comunicación serie se establece entre el puerto serie del HMI y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

**1. Conexión de hardware**

Cable de conexión:

RS232 (puerto serie, protocolo RS232)

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
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="3"><p><strong>Serie Hitachi E/EH</strong></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>RX</p></td>
<td><p>5</p></td>
<td colspan="2"><p>SD</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>TX</p></td>
<td><p>6</p></td>
<td colspan="2"><p>RD</p></td>
</tr>
<tr class="even">
<td><p>5</p></td>
<td><p>GND</p></td>
<td><p>1</p></td>
<td colspan="2"><p>SG</p></td>
</tr>
<tr class="odd">
<td colspan="2" rowspan="2"></td>
<td><p>4</p></td>
<td><p>PHL</p></td>
<td rowspan="2"><p>4-7</p>
<p>Cortocircuito</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>DR</p></td>
</tr>
</tbody>
</table>

|     |                                                      |     |                                                      |     |                                                     |
|-----|------------------------------------------------------|-----|------------------------------------------------------|-----|-----------------------------------------------------|
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     | <img src="../../drivers/hitachi.files/image002.gif" width="91" /> |
|     | <img src="../../drivers/hitachi.files/image003.gif" width="130" /> |     |                                                      |     |                                                     |
|     |                                                      |     | <img src="../../drivers/hitachi.files/image004.gif" width="278" /> |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |
|     |                                                      |     |                                                      |     |                                                     |

El conector del HMI de la serie HM es DB9F y el del equipo es RJ45.

**2. Ajustes de software**

Elija Hitachi Industrial en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Hitachi de la serie E/EH.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie Hitachi E/EH         | Serie Hitachi E/EH                          |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 7                           | 7/8                                          |
| **Paridad**              | EVEN                        | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                           | 1/2                                          |
| **Número de estación del PLC**      | 0                           | 0~255                                        |
| **Número de estación del HMI**      | 0                           | 0~255                                        |

|                         |                             |
|-------------------------|-----------------------------|
| **Función** | **Compatible** |
| **Simulación sin conexión** | Sí                         |
| **Simulación en línea**  | Sí                         |
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                                                    |
|-------------------|--------------------|-----------------|--------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                        |
| **X**             | hhhh               | 0~ffff          | Bit: Entrada digital externa, solo lectura                     |
| **Y**             | hhhh               | 0~ffff          | Bit: Salida digital externa |
| **M**             | hhhh               | 0~ffff          | Bit: Relé interno (marca)                                                |
| **R**             | hhhh               | 0~ffff          | Bit: Registro interno                                             |
| **T**             | hhhh               | 0~ffff          | Bit: Estado del temporizador                                               |
| **L**             | hhhh               | 0~ffff          | Bit: Relé de enlace                                                    |
| **WX**            | hhhh               | 0~ffff          | Palabra: Entrada digital externa                               |
| **WY**            | hhhh               | 0~ffff          | Palabra: Salida digital externa                              |
| **WM**            | hhhh               | 0~ffff          | Palabra: Relé interno (marca)                                               |
| **WR**            | hhhh               | 0~ffff          | Palabra: Registro interno                                            |
| **WL**            | hhhh               | 0~ffff          | Palabra: Relé de enlace                                                   |
| **TC**            | hhhh               | 0~ffff          | Palabra: Valor actual de temporizador/contador                               |

<img src="../../drivers/hitachi.files/image005.gif" width="595" />

Nota:

h: hexadecimal, rango de entrada 0-9, a-f;

Bit en las observaciones: el registro solo puede usarse como bit;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado.

<img src="../../drivers/hitachi.files/image006.gif" width="595" />
