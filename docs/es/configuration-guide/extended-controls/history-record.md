# Visualización de datos históricos

<span id="OLE_LINK279"></span><span id="OLE_LINK278"></span>         En la práctica, los datos del PLC u otros equipos conectados pueden cambiar en cualquier momento, como las alarmas. Para consultar datos históricos se usa el recopilador de datos históricos de CommandHMI.

CommandHMI ofrece la función de recopilador de datos históricos, accesible desde el gestor de proyecto. En un proyecto nuevo, haga clic con el botón derecho en «Recopilador de datos históricos» para añadir uno y después doble clic en «Recopilador de datos históricos 0» para configurarlo. Véanse las propiedades del «[Recopilador de datos históricos](../../setting/history-data.md)» en el capítulo 6.

Haga clic en el botón de visualización de datos históricos<img src="../../../configuration-guide/extended-controls/history-record.files/history-record687.png" width="32" /> de la barra de herramientas; se abre el cuadro de diálogo siguiente:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record747.png" width="579" />

Figura 4-65 Cuadro de diálogo Visualización de datos históricos

**General:**

• Color de primer plano: haga clic en el color del recuadro para cambiar el color de primer plano.

• Color del borde: haga clic en el color del recuadro para cambiar el color del borde.

• Título: tamaño y estilo de fuente, color de fondo, color del texto y si se muestran fecha y hora. Para el idioma, véase la «Visualización de alarmas».

• Datos: tamaño de fuente, color y número máximo de líneas mostradas.

Dirección de control:

Escriba 1 en el registro de offset 0 (entero de 16 bits, igual para 1 a 12), la hora de inicio en los registros de offset 1~6, la hora de fin en los registros 7~12 y por último 1 en el registro 13. La visualización de datos históricos muestra entonces los datos de ese periodo. El registro 13 se reinicia automáticamente. Para mostrar todos los datos históricos, escriba 0 en el registro 0.

Esta dirección ocupa 40 offsets consecutivos. Su significado es el siguiente:

|                |                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Offset de dirección | Elemento controlado por el registro de control                                                                                                                            |
| 0              | 1: muestra los datos entre la hora de inicio y la de fin; 0: muestra todos los datos.                                                                             |
| 1              | Hora de inicio (año); una palabra                                                                                                                                              |
| 2              | Hora de inicio (mes); una palabra                                                                                                                                             |
| 3              | Hora de inicio (día); una palabra                                                                                                                                               |
| 4              | Hora de inicio (hora); una palabra                                                                                                                                              |
| 5              | Hora de inicio (minuto); una palabra                                                                                                                                               |
| 6              | Hora de inicio (segundo); una palabra                                                                                                                                            |
| 7              | Hora de fin (año); una palabra                                                                                                                                                |
| 8              | Hora de fin (mes); una palabra                                                                                                                                               |
| 9              | Hora de fin (día); una palabra                                                                                                                                                 |
| 10             | Hora de fin (hora); una palabra                                                                                                                                                |
| 11             | Hora de fin (minuto); una palabra                                                                                                                                              |
| 12             | Hora de fin (segundo); una palabra                                                                                                                                              |
| 13             | Al pasar de 0 a 1 con el offset 0 a 1, se muestran los datos del periodo indicado; reinicio automático; <span id="OLE_LINK339"></span>una palabra |
| 14             | Número total de datos históricos entre la hora de inicio y la de fin; doble palabra                                                                                     |

Datos:

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record2617.png" width="581" />

Número de grupo: CommandHMI ofrece varios grupos de datos históricos a elegir.

Uso de la visualización de datos históricos: para mostrar los datos mediante las direcciones de control, la configuración es la de la figura 4-65-1:

<img src="../../../configuration-guide/extended-controls/history-record.files/001.png" width="797" />

Figura 4-65-1

Introduzca 1 en «Mostrar todos los datos» y 1 en «Consultar»: el recopilador muestra todos los datos históricos entre la hora de inicio y la de fin. Como en la figura 4-65-2

<img src="../../../configuration-guide/extended-controls/history-record.files/002.png" width="795" />

Figura 4-65-2

Introduzca 1 en «Mostrar todos los datos», hora de inicio 2016-7-11 3: 30: 4 y hora de fin 2016-7-11 14: 39: 4; al introducir 1 en «Consultar» solo se muestran los datos de ese periodo.

<img src="../../../configuration-guide/extended-controls/history-record.files/history-record3263.png" width="130" />

Para la página «Visibilidad», véase el objeto «Botón de bit».
