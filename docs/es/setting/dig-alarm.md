# Alarmas digitales

Los ajustes de alarmas sirven para mostrar las alarmas; sin ellos, la visualización de alarmas y la barra de alarmas no funcionan (muestran los mensajes de las alarmas digitales y analógicas).

Haga clic derecho en «Alarmas» en el gestor de proyecto y elija «Nueva alarma digital», como en la figura 7-22:

<img src="../../setting/dig-alarm.files/image001.jpg" width="274" alt="ScreenShot00094.jpg" />

Figura 7-22    Elegir el registro de alarmas

Haga doble clic en «Alarmas digitales» para abrir el cuadro de diálogo, como en la figura 7-23:

<img src="../../setting/dig-alarm.files/dig-alarm508.png" width="558" />

Figura 7-23    Elegir bits consecutivos

Para crear alarmas digitales:

• Introduzca primero la dirección de lectura; aquí se supone la dirección interna LB1.

• En la columna «Tamaño» (Size), elija el número total de alarmas, es decir, de direcciones de bit consecutivas. Aquí se supone 6.

• Ajuste el «Tiempo de exploración» (Scanning time) de las alarmas de bit, es decir, su frecuencia de lectura.

• Haga clic en un elemento de la lista y vaya a la zona «Mensaje» de la derecha; escriba el texto de la alarma en el campo «Texto». Aquí se suponen los mensajes de la figura 7-23.

• Si «Usar» está marcado, la alarma se muestra en la visualización de alarmas o en la barra de alarmas. Si no, el mensaje no aparece aunque la dirección valga 1. Si la dirección vale 0, la alarma no se muestra.

• Alarma en OFF: si se marca, la alarma se dispara cuando la dirección vale 0 (OFF); si no, cuando vale 1 (ON). Por defecto, alarma con 1 (ON).

• Exportar U: exporta los ajustes de alarmas

• Importar U: importa los ajustes de alarmas

Ejemplo con el tipo «Bits consecutivos»:

• Si LB1 vale 0, la alarma no aparece en la visualización de alarmas ni en la barra de alarmas, esté o no marcado «Usar».

• Si LB1 vale 1 y «Usar» no está marcado, la alarma no aparece en la visualización de alarmas ni en la barra de alarmas.

• Si LB1 vale 1 y «Usar» está marcado, la alarma aparece en la visualización de alarmas y en la barra de alarmas.

Haga clic en «Aceptar» para terminar. Añada 6 botones de bit con la función «Alternar» y las direcciones LB1-LB6, coloque una visualización de alarmas y una barra de alarmas en la pantalla y compruebe el resultado con la simulación sin conexión.

Ejemplo de simulación sin conexión, figura 7-24:

<img src="../../setting/dig-alarm.files/dig-alarm2644.png" width="1182" />

Figura 7-24    Simulación sin conexión de alarmas digitales

Con el tipo «Bits consecutivos de una palabra», como en la figura 7-25:

<img src="../../setting/dig-alarm.files/dig-alarm2789.png" width="559" />

Figura 7-25    Elegir bits consecutivos de una palabra

Si «Usar» está marcado para un número de bit, la alarma se dispara cuando ese bit vale 1.

<img src="../../setting/dig-alarm.files/dig-alarm2952.png" width="130" />

Nota: si copia los textos de alarma de otros documentos, compruebe que no contienen saltos de línea (invisibles). Es preferible escribirlos a mano para evitar errores de visualización.

Con el tipo «Valor de palabra», como en la figura 7-26:

<img src="../../setting/dig-alarm.files/dig-alarm3352.png" width="556" />

Figura 7-26    Cuadro de diálogo de alarma digital «Valor de palabra»

La alarma se dispara cuando el valor de la dirección es igual al valor elegido en la lista.

Coloque una visualización de alarmas de 7 líneas como en la figura 7-24 y una barra de alarmas dinámica con las propiedades de la figura 7-27:

<img src="../../setting/dig-alarm.files/dig-alarm3691.png" width="675" />

Figura 7-27    Propiedades de la barra de alarmas dinámica

Por último, añada seis botones de bit con las direcciones de escritura LB1-LB6 y las funciones «Alternar», «Monitorizar» y «Dirección de monitorización igual a la de escritura». Guarde el proyecto con «Guardar» en la barra de herramientas, elija «Offline» en el menú «Download» y haga clic en los botones LB1, LB2, LB4 y LB6: la visualización de alarmas y la barra de alarmas dinámica muestran las alarmas digitales de LB1, LB2, LB4 y LB6. Un nuevo clic pone los valores a 0 (función alternar) y ya no se muestra nada.

<img src="../../setting/dig-alarm.files/dig-alarm4400.png" width="130" />

Nota: con el cambio de idioma, cada idioma puede tener sus propios textos de alarma.

Nota: los HMI de la serie HM admiten como máximo 10 alarmas digitales.
