# Controlador Xinje

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Thinget XC/XCM/XD. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p>Cómo establecer la conexión con un PLC de la serie Thinget XC/XCM/XD</p>
<p><strong>1.  Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS232 <span id="OLE_LINK3"></span><span id="OLE_LINK2"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>Pantalla táctil COM1/COM2</strong></p></td>
<td colspan="2"><p><strong>Serie Thinget XC/XCM/XD</strong></p></td>
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
<td><p>8</p></td>
<td><p>GND</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/xinje.files/image006.gif" width="130" /><img src="../../drivers/xinje.files/image007.gif" width="280" /><img src="../../drivers/xinje.files/image008.gif" width="146" /></p></td>
</tr>
</tbody>
</table>

El conector del HMI es DB9F y el del PLC Thinget de la serie XC/XCM/XD es MD8M.

**2. Ajustes de software**

Elija Xinje Electronic en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Thinget de la serie XC/XCM/XD.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie Thinget XC           | Serie Thinget XC/XCM/XD                     |
| **Tipo de puerto** | RS232                       | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                       | 1200/2400/4800/9600/19200/38400/57600/115200 |
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
| **Modo extendido**       | Sí                         |

**3. Registros accesibles y rangos de direcciones**

Serie Thinget XC/XCM

|                   |                    |                 |                                    |
|-------------------|--------------------|-----------------|------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                        |
| **X**             | dddd               | 0 a 1037       | Bit: Bobina de entrada                    |
| **Y**             | dddd               | 0 a 1037       | Bit: Bobina de salida                   |
| **M**             | dddd               | 0 a 8767       | Bit: Bobina interna                 |
| **S**             | dddd               | 0 a 1023       | Bit: Etapa de proceso                       |
| **T**             | ddd                | 0 a 639        | Bit: Estado del temporizador                   |
| **C**             | ddd                | 0 a 639        | Bit: Estado del contador                 |
| **D**             | dddd               | 0 a 9023       | Palabra: Registro de datos                |
| **TD**            | ddd                | 0 a 639        | Palabra: Valor actual del temporizador   |
| **CD**            | ddd                | 0 a 639        | Palabra: Valor actual del contador |
| **FD**            | dddd               | 0 a 9023       | Palabra: Registro FlashROM            |
| **ED**            | ddddd              | 0 a 16383      | Palabra: Registro interno extendido   |

Serie Thinget XD2

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Nombre del registro</strong></p></td>
<td><p><strong>Formato de dirección</strong></p></td>
<td><p><strong>Rango de entrada</strong></p></td>
<td><p><strong>Observaciones</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>X</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Bobina de entrada</p></td>
</tr>
<tr class="odd">
<td><p><strong>Y</strong></p></td>
<td><p>o</p></td>
<td><p>0~7</p></td>
<td><p>Bobina de salida</p></td>
</tr>
<tr class="even">
<td><p><strong>M</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Relé interno (marca)</p></td>
</tr>
<tr class="odd">
<td><p><strong>HM</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~959</p></td>
<td><p>Relé interno (marca)</p></td>
</tr>
<tr class="even">
<td><p><strong>SM</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Relé interno especial</p></td>
</tr>
<tr class="odd">
<td><p><strong>S</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1023</p></td>
<td><p>Etapa de proceso</p></td>
</tr>
<tr class="even">
<td><p><strong>HS</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~127</p></td>
<td><p>Etapa de proceso</p></td>
</tr>
<tr class="odd">
<td><p><strong>T</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Temporizador</p></td>
</tr>
<tr class="even">
<td><p><strong>TD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Valor actual del temporizador</p></td>
</tr>
<tr class="odd">
<td><p><strong>HT</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Temporizador</p></td>
</tr>
<tr class="even">
<td><p><strong>ET</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Temporizador de precisión</p></td>
</tr>
<tr class="odd">
<td><p><strong>ETD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~31</p></td>
<td><p>Registro interno extendido</p></td>
</tr>
<tr class="even">
<td><p><strong>C</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Contador</p></td>
</tr>
<tr class="odd">
<td><p><strong>CD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~575</p></td>
<td><p>Valor actual del contador</p></td>
</tr>
<tr class="even">
<td><p><strong>HC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~95</p></td>
<td><p>Contador</p></td>
</tr>
<tr class="odd">
<td><p><strong> HSC</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Contador rápido</p></td>
</tr>
<tr class="even">
<td><p><strong>D</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~7999</p></td>
<td><p>Registro de datos</p></td>
</tr>
<tr class="odd">
<td><p><strong>HD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~999</p></td>
<td><p>Registro de datos</p></td>
</tr>
<tr class="even">
<td><p><strong>SD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~2047</p></td>
<td><p>Registro de datos especial</p></td>
</tr>
<tr class="odd">
<td><p><strong>HSD</strong></p></td>
<td><p>ddd</p></td>
<td><p>0~499</p></td>
<td><p>Registro de datos especial</p></td>
</tr>
<tr class="even">
<td><p><strong>FD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~4095</p></td>
<td><p>Registro FlashROM</p></td>
</tr>
<tr class="odd">
<td><p><strong>SFD</strong></p></td>
<td><p>dddd</p></td>
<td><p>0~1999</p></td>
<td><p>Registro FlashROM</p></td>
</tr>
<tr class="even">
<td><p><strong>FS</strong></p></td>
<td><p>dd</p></td>
<td><p>0~47</p></td>
<td><p>Registro de seguridad especial</p></td>
</tr>
<tr class="odd">
<td><p><strong>SEM</strong></p></td>
<td><p>dd</p></td>
<td><p>0~31</p></td>
<td><p>Bloque de función secuencial WAIT<br />
Bobina de comando</p></td>
</tr>
</tbody>
</table>

Serie Thinget XD3

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Bobina de entrada (X10000~X11177 pertenecen al módulo de ampliación) (X20000~X20277 al módulo de ampliación BD)              |
| **Y**             | ooooo              | 0~20077         | Bobina de salida (Y10000~Y11177 pertenecen al módulo de ampliación) (Y20000~Y20277 al módulo de ampliación BD) |
| **M**             | dddd               | 0~7999          | Relé interno (marca)                                                                                                   |
| **HM**            | ddd                | 0~959           | Relé interno (marca)                                                                                                   |
| **SM**            | dddd               | 0~2047          | Relé interno especial                                                                                           |
| **S**             | dddd               | 0~1023          | Etapa de proceso                                                                                            |
| **HS**            | ddd                | 0~127           | Etapa de proceso                                                                                            |
| **T**             | ddd                | 0~575           | Temporizador                                                                                                            |
| **TD**            | ddd                | 0~575           | Valor actual del temporizador                                                                                              |
| **HT**            | dd                 | 0~95            | Temporizador                                                                                                            |
| **ET**            | dd                 | 0~31            | Temporizador de precisión                                                                                                  |
| **ETD**           | ddd                | 0~31            | Registro interno extendido                                                                                       |
| **C**             | ddd                | 0~575           | Contador                                                                                                          |
| **CD**            | ddd                | 0~575           | Valor actual del contador                                                                                            |
| **HC**            | dd                 | 0~95            | Contador                                                                                                          |
| **HSC**          | dd                 | 0~31            | Contador rápido                                                                                               |
| **D**             | dddd               | 0~7999          | Registro de datos                                                                                                    |
| **HD**            | ddd                | 0~999           | Registro de datos                                                                                                    |
| **SD**            | dddd               | 0~2047          | Registro de datos especial                                                                                            |
| **HSD**           | ddd                | 0~499           | Registro de datos especial                                                                                            |
| **FD**            | dddd               | 0~4095          | Registro FlashROM                                                                                                |
| **SFD**           | dddd               | 0~1999          | Registro FlashROM                                                                                                |
| **FS**            | dd                 | 0~47            | Registro de seguridad especial                                                                                        |
| **ID**            | ddddd              | 0~20099         | Unidad base (ID10000~ID10999 pertenecen al módulo de ampliación) (ID20000~20099 al módulo de ampliación BD)              |
| **QD**            | ddddd              | 0~20099         | Unidad base (QD10000~QD10999 pertenecen al módulo de ampliación) (QD20000~QD20099 al módulo de ampliación BD)            |
| **SEM**           | dd                 | 0~31            | Bloque de función secuencial WAIT, bobina de comando                                                                      |

Serie Thinget XD5/XDM

|                   |                    |                 |                                                                                                                  |
|-------------------|--------------------|-----------------|------------------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                                      |
| **X**             | ooooo              | 0~20077         | Bobina de entrada (X10000~X11177 pertenecen al módulo de ampliación) (X20000~X20277 al módulo de ampliación BD)              |
| **Y**             | ooooo              | 0~20077         | Bobina de salida (Y10000~Y11177 pertenecen al módulo de ampliación) (Y20000~Y20277 al módulo de ampliación BD) |
| **M**             | ddddd              | 0~20479         | Relé interno (marca)                                                                                                   |
| **HM**            | ddddd              | 0~11999         | Relé interno (marca)                                                                                                   |
| **SM**            | dddd               | 0~4095          | Relé interno especial                                                                                           |
| **S**             | dddd               | 0~7999          | Etapa de proceso                                                                                            |
| **HS**            | ddd                | 0~999           | Etapa de proceso                                                                                            |
| **T**             | dddd               | 0~4095          | Temporizador                                                                                                            |
| **TD**            | ddd                | 0~575           | Valor actual del temporizador                                                                                              |
| **HT**            | dddd               | 0~1023          | Temporizador                                                                                                            |
| **ET**            | dd                 | 0~39            | Temporizador de precisión                                                                                                  |
| **ETD**           | ddd                | 0~39            | Registro interno extendido                                                                                       |
| **C**             | dddd               | 0~4095          | Contador                                                                                                          |
| **CD**            | ddd                | 0~4095          | Valor actual del contador                                                                                            |
| **HC**            | dddd               | 0~1023          | Contador                                                                                                          |
| **HSC**          | dd                 | 0~36            | Contador rápido                                                                                               |
| **D**             | ddddd              | 0~20479         | Registro de datos                                                                                                    |
| **HD**            | ddddd              | 0~6143          | Registro de datos                                                                                                    |
| **SD**            | dddd               | 0~4095          | Registro de datos especial                                                                                            |
| **HSD**           | dddd               | 0~1023          | Registro de datos especial                                                                                            |
| **FD**            | dddd               | 0~4095          | Registro FlashROM                                                                                                |
| **SFD**           | dddd               | 0~5999          | Registro FlashROM                                                                                                |
| **FS**            | dd                 | 0~47            | Registro de seguridad especial                                                                                        |
| **ID**            | ddddd              | 0~20099         | Unidad base (ID10000~ID10999 pertenecen al módulo de ampliación) (ID20000~20099 al módulo de ampliación BD)              |
| **QD**            | ddddd              | 0~20099         | Unidad base (QD10000~QD10999 pertenecen al módulo de ampliación) (QD20000~QD20099 al módulo de ampliación BD)            |
| **SEM**           | ddd                | 0~127           | Bloque de función secuencial WAIT, bobina de comando                                                                      |

<img src="../../drivers/xinje.files/image009.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/xinje.files/image011.gif" width="595" />
