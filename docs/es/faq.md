# Preguntas frecuentes y soluciones

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
<td><p>       <strong>No.</strong></p></td>
<td colspan="2"><p><strong>Síntoma</strong></p></td>
<td><p><strong>Causa</strong></p></td>
<td><p><strong>Solución</strong></p></td>
</tr>
<tr class="even">
<td rowspan="6"><p><strong>Pantalla</strong></p></td>
<td rowspan="5"><p>Pantalla negra</p></td>
<td rowspan="3"><p>Pantalla negra al encender</p></td>
<td><p>Problemas de alimentación</p></td>
<td><p>1、Compruebe la conexión de la alimentación; 2、Compruebe el tipo de alimentación; cámbiela si no es una fuente independiente de 24 V CC (±20 %).</p></td>
</tr>
<tr class="odd">
<td><p>Error en el proyecto, p. ej. scripts mal utilizados: puntero nulo, puntero no válido, desbordamiento de array o división por 0.</p></td>
<td><p>Ponga el interruptor DIP 2 en ON y vuelva a descargar el proyecto para probar; si un script falla, depúrelo y prográmelo correctamente.</p></td>
</tr>
<tr class="even">
<td><p>Avería del equipo: corrosión del cable plano del LCD, problema del oscilador de cuarzo, etc.</p></td>
<td><p>Contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="odd">
<td rowspan="2"><p>Pantalla negra repentina en funcionamiento, o pantalla negra o bloqueo ocasional</p></td>
<td><p>Problema de alimentación</p></td>
<td><p>Compruebe el cable y la fuente de alimentación.</p></td>
</tr>
<tr class="even">
<td><p>Avería del equipo</p></td>
<td><p>Contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Líneas en la pantalla, verticales u horizontales</p></td>
<td><p>Avería del LCD</p></td>
<td><p>Si las líneas aparecen en todas las pantallas, contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="even">
<td rowspan="4"><p><strong>Táctil</strong></p></td>
<td colspan="2" rowspan="2"><p>Respuesta táctil lenta, objetos difíciles de accionar</p></td>
<td><p>Problema de montaje</p></td>
<td><p>1. Compruebe si el recorte de montaje es demasiado pequeño y aprieta el HMI; en tal caso, móntelo con el recorte correcto; 2. Compruebe si los tornillos de fijación están demasiado apretados y procure una presión lo más uniforme posible en las cuatro esquinas.</p></td>
</tr>
<tr class="odd">
<td><p>Proyecto inadecuado</p></td>
<td><p>Demasiados datos de proyecto, scripts en segundo plano y demasiadas variables y objetos en las pantallas; revise el proyecto y reparta o reduzca razonablemente objetos y pantallas.</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>Fallo táctil</p></td>
<td><p>Calibración de coordenadas o panel táctil dañado</p></td>
<td><p>1. Ponga el interruptor DIP 1 en ON y ejecute la calibración de coordenadas;</p>
<p>2. <span id="OLE_LINK4"></span><span id="OLE_LINK3"></span>Si no se soluciona, contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Asignación errónea (en el teclado se pulsa A pero aparece X u otro carácter)</p></td>
<td><p>Avería del panel táctil</p></td>
<td><p>Contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="even">
<td rowspan="9"><p><strong>Fallo de comunicación</strong></p></td>
<td rowspan="6"><p>Corte de comunicación entre el HMI y el controlador</p></td>
<td rowspan="3"><p>La comunicación nunca funciona</p></td>
<td><p>Avería de los equipos de comunicación (PLC, microcontrolador, etc.)</p></td>
<td><p>Compruebe el estado del puerto de comunicación y vuelva a ajustar los parámetros de comunicación.</p></td>
</tr>
<tr class="odd">
<td><p>Avería del puerto de comunicación del HMI</p></td>
<td><p>Contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="even">
<td><p>Cable de comunicación cortado</p></td>
<td><p>Utilice en lo posible el cable original de CommandHMI.</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>Interrupción de la comunicación tras un tiempo de funcionamiento normal</p></td>
<td><p>Corrosión y oxidación en las conexiones del cable de comunicación tras un uso prolongado.</p></td>
<td><p>Sustituya el cable de comunicación o vuelva a soldarlo.</p></td>
</tr>
<tr class="even">
<td><p>Interferencias del entorno</p></td>
<td><p>Apantalle las fuentes de interferencia; use cable apantallado; conecte correctamente a tierra</p></td>
</tr>
<tr class="odd">
<td><p>Avería del HMI (por campos magnéticos o corrientes intensas o por un rayo en la instalación)</p></td>
<td><p>Contacte con el servicio posventa para la reparación en fábrica.</p></td>
</tr>
<tr class="even">
<td colspan="2" rowspan="3"><p>El HMI no se conecta al PC y no es posible descargar.</p></td>
<td><p>Controlador USB del PC mal instalado</p></td>
<td><p>Elija el controlador adecuado para el sistema operativo y reinstale el controlador USB.</p></td>
</tr>
<tr class="odd">
<td><p>El tamaño y el modelo del HMI no coinciden con el equipo real.</p></td>
<td><p>Seleccione el modelo de HMI correcto en el software de configuración.</p></td>
</tr>
<tr class="even">
<td><p>Puerto de descarga del HMI dañado</p></td>
<td><p>Contacte con el servicio posventa para la reparación en fábrica. (Comprobación: conecte otro HMI con el mismo cable USB y el mismo PC; si la descarga funciona, el fallo está en el puerto USB del HMI.)</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p><strong>Aplicación</strong></p></td>
<td colspan="2"><p>El proyecto no funciona</p></td>
<td><p>Objeto o script no válido en el proyecto</p></td>
<td><p>Corrija el proyecto</p></td>
</tr>
<tr class="even">
<td colspan="2"><p>El script no compila</p></td>
<td><p>Directorio de instalación de HM en las variables de entorno</p></td>
<td><p>Coloque el directorio de instalación de CommandHMI al principio de las variables de entorno.</p></td>
</tr>
<tr class="odd">
<td colspan="2"><p>Las simulaciones sin conexión y en línea no funcionan.</p></td>
<td><p>Ejecución sin derechos de administrador</p></td>
<td><p>Ejecute CommandHMI como administrador</p></td>
</tr>
</tbody>
</table>
