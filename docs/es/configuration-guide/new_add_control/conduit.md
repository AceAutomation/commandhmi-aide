# Tubería

Este objeto dibuja una tubería con el diámetro definido, en la posición indicada

<img src="../../../configuration-guide/new_add_control/conduit.files/image004.jpg" width="488" alt="ScreenShot00831.jpg" />

Cuadro de diálogo general de la tubería

Ø  Estilo: estilo de visualización de la línea; los efectos posibles se muestran en «[estilo](#style)»

Ø Degradado: efecto de visualización de la tubería; los resultados posibles se muestran en «[degradado](#Graduallayer)»

Ø Diámetro: diámetro de la tubería «[diámetro](#diameter)».

Ø Espesor: espesor de la pared de la tubería, que se añade al diámetro. Véase el efecto en «[espesor](#thickness)»

Ø Borde: color del espesor de la tubería; es el color del borde cuando el espesor es 0

Ø  Pared/contenido: color principal de la tubería

Ø Color variable de pared/contenido

<img src="../../../configuration-guide/new_add_control/conduit.files/image005.jpg" width="451" alt="ScreenShot00832.jpg" />

l  Color de vista previa: con la función de color variable de pared/contenido activada, color mostrado por la línea, elegido entre pared/contenido, color de pared/contenido \# 2 y color de pared/contenido \# 3; solo se muestra en el software de configuración; en funcionamiento real, el color lo controlan los bits de la palabra de control

l  Color de pared/contenido \# 2, color de pared/contenido \# 3: colores alternativos de la línea

l  Control de parpadeo: controla el parpadeo de la línea

Ø  Control de flujo:

l  Palabra de control: palabra o doble palabra

l  Efecto de flujo: (solo se aplica a las tuberías para las que se ha activado el efecto de flujo en la página «Tubería»).

Tipo predefinido: efecto de flujo de la tubería

Color predefinido: color del flujo de la tubería

Relación de longitud predefinida (7): relación de longitud del flujo

Usar el tipo, color y longitud predefinidos para todas: aplica un tipo a todas las tuberías con efecto de flujo activado en la página «Tubería»

Ø Palabra de control:

<img src="../../../configuration-guide/new_add_control/conduit.files/image006.jpg" width="450" alt="ScreenShot00833.jpg" />

Cuando el usuario activa el color variable de pared/contenido y el control del efecto de flujo, cada bit del registro elegido controla un efecto distinto. Ejemplo con lw0

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Registro</strong></p></td>
<td><p><strong>N.º 0</strong></p></td>
<td><p><strong>N.º 1</strong></p></td>
<td><p><strong>N.º 2</strong></p></td>
<td><p><strong>N.º 3</strong></p></td>
<td><p><strong>N.º 4</strong></p></td>
<td><p><strong>N.º 5</strong></p></td>
<td><p><strong>N.º 6</strong></p></td>
<td><p><strong>N.º 7</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>LW0</strong></p>
<p><strong>（acción cuando el bit correspondiente está en ON）</strong></p></td>
<td><p>Color de la pared</p>
<p>Color de pared/contenido #3</p></td>
<td><p>Color de la pared</p>
<p>Color de pared/contenido #3</p></td>
<td><p>Parpadeo de la línea</p>
<p>Si los dos bits anteriores están ambos en ON u OFF, el color es el de pared/contenido definido</p>
<p>Si solo uno de los dos está activado, el color de la línea alterna con el color de contenido #</p></td>
<td><p>Flujo en la tubería</p></td>
<td><p>reservado</p></td>
<td><p>reservado</p></td>
<td><p>reservado</p></td>
<td><p>reservado</p></td>
</tr>
</tbody>
</table>

Página de ajuste de la tubería:

<img src="../../../configuration-guide/new_add_control/conduit.files/image007.jpg" width="488" alt="ScreenShot00834.jpg" />

Ø  Página de ajuste de la tubería

l  X1，Y1，X2，Y2：

Coordenadas de la tubería: coordenada izquierda (x1,y1), coordenada derecha (x2, y2).

El usuario puede modificar las coordenadas con cuidado: en un tramo horizontal solo puede modificarse la coordenada x y en uno vertical solo la y; las coordenadas de los codos no pueden modificarse, pero sí su estilo.

l  Efecto de flujo: el usuario puede definir para cada tubería un tipo de efecto de flujo, un color, una relación de longitud, etc.

Si el usuario usa el mismo efecto para todas, basta con activar aquí el efecto de flujo y usar los ajustes predefinidos de la página general, que se aplican a todas las tuberías del objeto con efecto de flujo activado.

La página de visualización es igual a la de los demás objetos; véase la página de visualización del «botón de bit».

<span id="style"></span>Estilo:

estilo 1<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="172" alt="ScreenShot00835.jpg" /> estilo 2<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="178" alt="ScreenShot00836.jpg" /> estilo 3<img src="../../../configuration-guide/new_add_control/conduit.files/image008.jpg" width="179" alt="ScreenShot00495.jpg" /> estilo 4<img src="../../../configuration-guide/new_add_control/conduit.files/image009.jpg" width="177" alt="ScreenShot00496.jpg" /> estilo 5<img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="187" alt="2019_7_30_11_37_36.jpg" />

<span id="Graduallayer"></span>Degradado:

Color sólido <img src="../../../configuration-guide/new_add_control/conduit.files/image011.jpg" width="182" alt="ScreenShot00498.jpg" /> Estilo 3D 1<img src="../../../configuration-guide/new_add_control/conduit.files/image012.jpg" width="180" alt="ScreenShot00499.jpg" /> Estilo 3D 2<img src="../../../configuration-guide/new_add_control/conduit.files/image013.jpg" width="180" alt="ScreenShot00500.jpg" /> Estilo 3D 3<img src="../../../configuration-guide/new_add_control/conduit.files/image014.jpg" width="179" alt="ScreenShot00501.jpg" />

<span id="diameter"></span>Diámetro:

diámetro 10<img src="../../../configuration-guide/new_add_control/conduit.files/image015.jpg" width="157" alt="ScreenShot00506.jpg" /> diámetro 20<img src="../../../configuration-guide/new_add_control/conduit.files/image016.jpg" width="188" alt="ScreenShot00507.jpg" /> diámetro 30<img src="../../../configuration-guide/new_add_control/conduit.files/image017.jpg" width="220" alt="ScreenShot00508.jpg" />

<span id="thickness"></span>Espesor:

espesor 0<img src="../../../configuration-guide/new_add_control/conduit.files/image018.jpg" width="183" alt="ScreenShot00502.jpg" /> espesor 1<img src="../../../configuration-guide/new_add_control/conduit.files/image019.jpg" width="174" alt="ScreenShot00505.jpg" /> espesor 4<img src="../../../configuration-guide/new_add_control/conduit.files/image020.jpg" width="178" alt="ScreenShot00503.jpg" /> espesor 8<img src="../../../configuration-guide/new_add_control/conduit.files/image021.jpg" width="187" alt="ScreenShot00504.jpg" />
