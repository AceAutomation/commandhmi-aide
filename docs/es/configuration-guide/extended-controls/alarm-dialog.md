# Visualización de alarmas históricas

La visualización de alarmas históricas muestra las alarmas pasadas; se usa igual que la visualización de alarmas. Haga clic en el botón de alarmas históricas <img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog791.png" width="32" /> de la barra de herramientas para abrir el cuadro de diálogo siguiente:

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog1031.png" width="650" />

Dirección de control: escriba 1 en el registro de offset 0 (entero de 16 bits, igual para 1 a 12), la hora de inicio en los registros de offset 1~6 y la hora de fin en los registros 7~12. La visualización de alarmas históricas muestra entonces los datos de ese periodo. Para mostrar todas las alarmas históricas, escriba 0 en el registro 0. El registro de offset 13 no se usa por ahora.

Esta dirección ocupa 12 offsets consecutivos; su significado es el siguiente:

|                |                                                                                              |
|----------------|----------------------------------------------------------------------------------------------|
| Offset de dirección | Elemento controlado por el registro de control                                                |
| 0              | 1: muestra los datos entre la hora de inicio y la de fin; 0: muestra todos los datos. |
| 1              | Hora de inicio (año)                                                                            |
| 2              | Hora de inicio (mes)                                                                           |
| 3              | Hora de inicio (día)                                                                             |
| 4              | Hora de inicio (hora)                                                                           |
| 5              | Hora de inicio (minuto)                                                                             |
| 6              | Hora de inicio (segundo)                                                                          |
| 7              | Hora de fin (año)                                                                              |
| 8              | Hora de fin (mes)                                                                             |
| 9              | Hora de fin (día)                                                                               |
| 10             | Hora de fin (hora)                                                                              |
| 11             | Hora de fin (minuto)                                                                            |
| 12             | Hora de fin (segundo)                                                                            |

• Borrar fecha de alarma: oculta la fecha de la alarma

• Borrar hora de alarma: oculta la hora de la alarma

• Borrar alarma: la línea de una alarma borrada se marca con este color

• Estadística de alarmas: activa el recuento de alarmas, que se muestra tras el mensaje.

• Tiempo acumulado: activa el tiempo acumulado de la alarma, que se muestra tras el mensaje.

• OK: la alarma se indica con este color cuando se produce

<img src="../../../configuration-guide/extended-controls/alarm-dialog.files/alarm-dialog2576.png" width="130" />

Para el uso básico, véase el objeto «Visualización de alarmas».

Para la página «Visibilidad», véase el objeto «Botón de bit».
