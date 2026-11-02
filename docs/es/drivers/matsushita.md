# Controlador Matsushita

Este controlador permite a los HMI de la serie HM leer y escribir datos o estados de los registros de los PLC Matsushita de la serie FP. La comunicación serie se establece entre el puerto serie de la pantalla táctil y el del PLC. Antes de usar este controlador, lea atentamente este capítulo y la documentación técnica del PLC.

Cómo establecer la conexión con un PLC Matsushita de la serie FP

**1.  Conexión de hardware**

Cable de conexión:

RS232-FP0/FP2/FP2SH/FPM

|                                                                                                                                                 |     |                          |     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----|--------------------------|-----|
| **HMI serie HM COM1/COM2** |     | **Serie Matsushita FP** |     |
| 2                                                                                                                                               | RX  | 3                        | TX  |
| 3                                                                                                                                               | TX  | 2                        | RX  |
| 5                                                                                                                                               | GND | 1                        | GND |

<img src="../../drivers/matsushita.files/image002.gif" width="280" /><img src="../../drivers/matsushita.files/image003.gif" width="129" /><img src="../../drivers/matsushita.files/image004.gif" width="145" />

El conector del HMI es DB9F y el del PLC Matsushita de la serie FP es MD5M.

RS422-FP1

|                             |     |                      |     |
|-----------------------------|-----|----------------------|-----|
| **HMI serie HM COM1/COM2** |     | Serie Matsushita FP |     |
| 6                           | RX- | 2                    | TX- |
| 7                           | RX+ | 5                    | TX+ |
| 8                           | TX- | 3                    | RX- |
| 9                           | TX+ | 6                    | RX+ |

<img src="../../drivers/matsushita.files/image005.gif" width="140" /><img src="../../drivers/matsushita.files/image006.gif" width="129" /><img src="../../drivers/matsushita.files/image007.gif" width="280" />

El conector del HMI es DB9F y el del PLC Matsushita de la serie FP es MD8M.

**2. Ajustes de software**

Elija MATSUSHITA en el servicio de equipo de la conexión.

Elija la opción correspondiente del servicio de equipo según el modelo de PLC conectado o el protocolo admitido.

Compruebe que los parámetros de comunicación de la pantalla táctil y el número de estación del PLC coinciden con los del PLC conectado.

Para la configuración del PLC conectado, consulte la documentación técnica de los PLC Matsushita de la serie FP.

Parámetros de conexión por defecto de los HMI de la serie HM

|                             |                             |                                              |
|-----------------------------|-----------------------------|----------------------------------------------|
| **Parámetro**            | **Valor por defecto** | **Rango de ajuste**                            |
| **Tipo de PLC**                | Serie FP                   | Serie FP                                    |
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
| **Modo extendido**       | No                          |

**3. Registros accesibles y rangos de direcciones**

|                   |                    |                 |                                        |
|-------------------|--------------------|-----------------|----------------------------------------|
| **Nombre del registro** | **Formato de dirección** | **Rango de entrada** | **Observaciones**                            |
| **X**             | ddddh              | 0~9999f         | Bit: Entrada externa, solo lectura         |
| **Y**             | ddddh              | 0~9999f         | Bit: Salida externa                   |
| **R**             | ddddh              | 0~9999f         | Bit: Relé interno (marca)                    |
| **L**             | ddddh              | 0~9999f         | Bit: Relé de enlace                        |
| **T**             | dddd               | 0~9999          | Bit: Estado del temporizador, solo lectura        |
| **C**             | dddd               | 0~9999          | Bit: Estado del contador, solo lectura      |
| **WX**            | dddd               | 0~9999          | Palabra: Entrada externa, solo lectura        |
| **WY**            | dddd               | 0~9999          | Palabra: Salida externa                  |
| **WR**            | dddd               | 0~9999          | Palabra: Relé interno (marca)                   |
| **WL**            | dddd               | 0~9999          | Palabra: Relé de enlace                       |
| **DT**            | ddddd              | 0~99999         | Palabra: Registro de datos                    |
| **LD**            | ddddd              | 0~99999         | Palabra: Registro de enlace                    |
| **FL**            | ddddd              | 0~99999         | Palabra: Registro de archivo                    |
| **SV**            | dddd               | 0~9999          | Palabra: Área de consignas de temporizadores/contadores     |
| **EV**            | dddd               | 0~9999          | Palabra: Área de valores actuales de temporizadores/contadores |

<img src="../../drivers/matsushita.files/image008.gif" width="595" />

Nota:

d: decimal, rango de entrada 0-9;

h: hexadecimal, rango de entrada 0-9, a-f;

Palabra en las observaciones: el registro solo puede usarse como palabra;

Bit en las observaciones: el registro solo puede usarse como bit;

Solo lectura en las observaciones: el registro puede leerse pero no escribirse;

Los nombres y rangos de los registros pueden variar según el modelo de equipo.

Para los nombres y rangos exactos, consulte la documentación técnica del equipo conectado

<img src="../../drivers/matsushita.files/image009.gif" width="595" />
