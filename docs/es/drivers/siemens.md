# Controlador Siemens

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC de la serie Siemens S7-200/300/1200. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.</p></td>
</tr>
<tr class="even">
<td><p> Cómo establecer la conexión con un PLC de la serie Siemens S7-200/300/1200tcp</p>
<p><strong>1. 1 Conexión de hardware</strong></p>
<p>Cable de conexión:</p>
<p>RS485-Siemens S7-200<span id="OLE_LINK1"></span><span id="OLE_LINK2"></span><span id="OLE_LINK3"></span></p>
<table>
<tbody>
<tr class="odd">
<td colspan="2"><p><strong>HMI serie HM COM1/COM2</strong></p></td>
<td colspan="2"><p>Serie Siemens S7-200</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>TX-</p></td>
<td><p>8</p></td>
<td><p>TX-</p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>TX+</p></td>
<td><p>3</p></td>
<td><p>TX+</p></td>
</tr>
</tbody>
</table>
<p><img src="../../drivers/siemens.files/image002.gif" width="130" /><img src="../../drivers/siemens.files/image003.gif" width="290" /><img src="../../drivers/siemens.files/image004.gif" width="130" /></p></td>
</tr>
</tbody>
</table>

  RS232-Siemens S7-300

|                             |     |                           |     |
|-----------------------------|-----|---------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Serie Siemens S7-300** |     |
| **2**                       | RX  | 3                         | TX  |
| **3**                       | TX  | 2                         | RX  |
| **5**                       | GND | 5                         | GND |

|     |                                                      |     |                                                      |
|-----|------------------------------------------------------|-----|------------------------------------------------------|
|     |                                                      |     |                                                      |
|     | <img src="../../drivers/siemens.files/image005.gif" width="408" /> |     | <img src="../../drivers/siemens.files/image006.gif" width="129" /> |

El conector del HMI es DB9F y el puerto MPI del PLC Siemens de la serie S7-300 es DB9M.

Cómo establecer la conexión con un PLC Siemens de la serie S7-200/300/1200

**1. 2 Conexión de hardware**

Cable de conexión:

  Cable RJ45;

  Pines del RJ45:

**<img src="../../drivers/siemens.files/image014.jpg" width="343" />**

1、 Ajuste de la IP y el número de puerto

En la página «General» de las propiedades del puerto de comunicación, elija «Puerto Ethernet» como interfaz de conexión y «SIEMENS», «Siemens S7-200(TCP/IP)/Siemens S7-300(TCP/IP)/Siemens S7-1200(TCP)» como servicio de conexión;

En la página «Parámetros» de las propiedades del puerto de comunicación, defina la IP y el número de puerto.

Atención:

Las direcciones IP del PLC y del HMI deben estar en la misma subred; basta con ajustar la máscara de subred a 255.255.255.0.

2、 En la configuración del PLC Siemens 1200, compruebe si el PLC tiene activada la protección de conexión; si es necesario, marque la opción correspondiente y vuelva a compilar y descargar el programa al PLC.

Cargue el programa del PLC o cree uno nuevo para Siemens 1200 en TIA Portal; haga clic derecho en el equipo y elija «Propiedades»; en «Protección», marque «Permitir acceso vía comunicación PUT/GET del interlocutor remoto (PLC, HMI, OPC...)», como en la figura siguiente:

**<img src="../../drivers/siemens.files/image015.jpg" width="1152" />**

**2. Ajustes de software**

Elija SIEMENS en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Siemens de la serie S7-200/300

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                         |                                    |                                              |
|-----------------------------|-------------------------|------------------------------------|----------------------------------------------|
| **Parámetro**            | Valor por defecto |                                    | Rango de ajuste                                |
| **Tipo de PLC**                | S7-200(PPI)             |                                    | S7-200(PPI)/ S7-300(MPI)                     |
| **Tipo de puerto** | RS485                   |                                    | RS232/RS422/RS485                            |
| **Velocidad (baudios)**               | 19200                   |                                    | 1200/2400/4800/9600/19200/38400/57600/115200 |
| **Bits de datos**         | 8                       |                                    | 7/8                                          |
| **Paridad**              | EVEN                    |                                    | EVEN/ODD/NONE                                |
| **Bits de parada**         | 1                       |                                    | 1/2                                          |
| **Número de estación del PLC**      | 2                       |                                    | 1 a 255                                     |
| **Número de estación del HMI**      | 0                       |                                    | 0 a 255                                     |
| **Función**     |                         | **Compatible**        |                                              |
| **Simulación sin conexión**     |                         | Sí                                |                                              |
| **Simulación en línea**      |                         | Sí                                |                                              |
| **Modo extendido**           |                         | Yes: S7-200(PPI)/ No.: S7-300(MPI) |                                              |
|                             |                         |                                    |                                              |

**3. Registros accesibles y rangos de direcciones**

Siemens S7-200

|                   |                    |                 |                                                                                                    |
|-------------------|--------------------|-----------------|----------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                                                                                        |
| **I**             | dd.o               | 0.0 a 4095.7   | Bit: Imagen de entradas, solo lectura                                                              |
| **Q**             | dd.o               | 0.0 a 4095.7   | Bit: Imagen de salidas                                                                        |
| **M**             | dd.o               | 0.0 a 4095.7   | Bit: Memoria de bits (marcas)                                                                                    |
| **S**             | dd.o               | 0.0 a 4095.7   | Bit: Relé de control secuencial                                                                        |
| **SM**            | ddd.o              | 0.0 a 4095.7   | Bit: Memoria de bits especial, SM0.0-SM29.7 solo lectura                                                    |
| **T**             | ddd                | 0 a 255        | Bit: Estado del temporizador: solo lectura                                                                        |
| **C**             | ddd                | 0 a 255        | Bit: Estado del contador: solo lectura                                                                      |
| **VB_Bit**        | ddddd.o            | 0.0 a 10239.7  | Bit: Bit de la memoria de variables                                                                           |
| **IW**            | dd                 | 0 a 4095       | Palabra: Imagen de entradas, solo lectura, registro de 8 bits, cada palabra ocupa dos direcciones         |
| **QW**            | dd                 | 0 a 4095       | Palabra: Imagen de salidas, registro de 8 bits, cada palabra ocupa dos direcciones                   |
| **MW**            | dd                 | 0 a 4095       | Palabra: Memoria de bits (marcas), registro de 8 bits, cada palabra ocupa dos direcciones                               |
| **SW**            | dd                 | 0 a 4095       | Palabra: Relé de control secuencial, registro de 8 bits, cada palabra ocupa dos direcciones                   |
| **SMW**           | ddd                | 0 a 4095       | Palabra: Memoria de bits especial, SMW0-SMW29 solo lectura, registro de 8 bits, cada palabra ocupa dos direcciones |
| **VB**            | ddddd              | 0 a 10239      | Palabra: Memoria de variables, registro de 8 bits                                                            |
| **VW**            | ddddd              | 0 a 10238      | Palabra: Memoria de variables, registro de 8 bits, cada palabra ocupa dos direcciones                          |
| **VD**            | ddddd              | 0 a 10236      | Doble palabra: Memoria de variables, registro de 8 bits, cada doble palabra ocupa cuatro direcciones           |
| **TV**            | ddd                | 0 a 255        | Palabra: Valor actual del temporizador                                                                   |
| **CV**            | ddd                | 0 a 255        | Palabra: Valor actual del contador                                                                 |
| **AIW**           | dd                 | 0 a 62         | Palabra: Entrada analógica, solo lectura, registro de 8 bits, cada palabra ocupa dos direcciones                  |
| **AQW**           | dd                 | 0 a 62         | Palabra: Salida analógica, solo escritura, registro de 8 bits, cada palabra ocupa dos direcciones                |

Siemens S7-300 / Siemens S7-300(MPI) / Siemens S7-300tcp

|                   |                    |                     |                                                                                                                                                            |
|-------------------|--------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada**     | **Observaciones**                                                                                                                                                |
| **I**             | dddd.o             | 0.0 a 4095.7       | Bit: Imagen de entradas                                                                                                                                 |
| **Q**             | dddd.o             | 0.0 a 4095.7       | Bit: Imagen de salidas                                                                                                                                |
| **M**             | dddd.o             | 0.0 a 4095.7       | Bit: Memoria de bits (marcas)                                                                                                                                            |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0 a 255:8192.7 | Bit: Bit de una palabra del área de bloques DB, número de bloque DD 0 a 255, palabra por bloque dddd 0 a 8192, bit por palabra o 0 a 7                          |
| **IW**            | dddd               | 0 a 4095           | Palabra: Imagen de entradas, registro de 8 bits, cada palabra ocupa dos direcciones                                                                            |
| **QW**            | dddd               | 0 a 4095           | Palabra: Imagen de salidas, registro de 8 bits, cada palabra ocupa dos direcciones                                                                           |
| **MW**            | dddd               | 0 a 4095           | Palabra: Memoria de bits (marcas), registro de 8 bits, cada palabra ocupa dos direcciones                                                                                       |
| **DBW**           | DDD:dddd           | 0:0 a 255:8192     | Palabra: Área de bloques DB, número de bloque DD 0 a 255, palabra dddd 0 a 8192, registro de 8 bits, cada palabra ocupa dos direcciones                |
| **DBD**           | DDD:dddd           | 0:0 a 255:8192     | Doble palabra: Área de bloques DB, número de bloque DD 0 a 255, palabra dddd 0 a 8192, registro de 8 bits, cada doble palabra ocupa cuatro direcciones |

Siemens S7-1200tcp

|                   |                    |                  |                                                                                                                                                            |
|-------------------|--------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada**  | **Observaciones**                                                                                                                             |
| **I**             | dddd.o             | 0.0~1024.7       | Bit: Imagen de entradas                                                                                                                                 |
| **Q**             | dddd.o             | 0.0~1024.7       | Bit: Imagen de salidas                                                                                                                                |
| **M**             | dddd.o             | 0.0~8191.7       | Bit: Memoria de bits (marcas)                                                                                                                                            |
| **DB_Bit**        | DDD:dddd.o         | 0:0.0~255:8192.7 | Bit: Bit de una palabra del área de bloques DB, número de bloque DD 0 a 255, palabra por bloque dddd 0 a 8192, bit por palabra o 0 a 7                          |
| **IW**            | dddd               | 0~1024           | Palabra: Imagen de entradas, registro de 8 bits, cada palabra ocupa dos direcciones                                                                            |
| **QW**            | dddd               | 0~1024           | Palabra: Imagen de salidas, registro de 8 bits, cada palabra ocupa dos direcciones                                                                           |
| **MW**            | dddd               | 0~8191           | Palabra: Memoria de bits (marcas), registro de 8 bits, cada palabra ocupa dos direcciones                                                                                       |
| **DBW**           | DDD:dddd           | 0:0~255:8192     | Palabra: Área de bloques DB, número de bloque DD 0 a 255, palabra dddd 0 a 8192, registro de 8 bits, cada palabra ocupa dos direcciones                |
| **DBD**           | DDD:dddd           | 0:0~255:8192     | Doble palabra: Área de bloques DB, número de bloque DD 0 a 255, palabra dddd 0 a 8192, registro de 8 bits, cada doble palabra ocupa cuatro direcciones |

LOGO_TCP

|                   |                    |                 |                                |
|-------------------|--------------------|-----------------|--------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones** |
| **I**             | dd                 | 1~64            | Bit: Imagen de entradas     |
| **Q**             | dd                 | 1~64            | Bit: Imagen de salidas    |
| **M**             | ddd                | 1~112           | Bit: Memoria de bits (marcas)                |
| **VB**            | dddd.o             | 0.0~1023.7      | Bit                            |
| **AI**            | dd                 | 1~16            | Palabra: Imagen de entradas    |
| **AQ**            | dd                 | 1~16            | Palabra: Imagen de salidas   |
| **AM**            | dd                 | 1~64            | Palabra: Memoria de bits (marcas)               |
| **VW**            | dddd               | 0~511           | Word                           |

<img src="../../drivers/siemens.files/image007.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

o: octal, rango de entrada 0-7;

DDD: número de bloque; rango de entrada 0-255;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Doble palabra en las observaciones: el tipo de dato del registro en el proyecto debe ser de 32 bits;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/siemens.files/image008.gif" width="595" />
