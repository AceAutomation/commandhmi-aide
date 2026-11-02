# Visualización de trayectorias

Este objeto dibuja elementos gráficos: puntos, líneas, arcos, círculos, etc.

Todas las direcciones que usa son registros internos LB o LW

Cuadro de diálogo general de visualización de trayectorias

• Color de primer plano, color del borde, color de fondo, visibilidad, estilo: véase el «botón de bit»

• Zona de definición de la trayectoria: zona donde se definen los elementos de la trayectoria; el significado de los datos se detalla al final del capítulo, en «[direcciones de la zona de definición de la trayectoria](#路径定义区地址说明)»

• Bit de dibujo: cuando el bit está en ON se inicia el dibujo; en OFF no

• Bit de borrado: en ON se borra el dibujo

• Función de selección: selecciona el gráfico dibujado para mostrar su información

• Controlado por bit: activa o no la función de selección; por defecto la dirección está en OFF y la selección está activada; con el bit en ON la selección se desactiva

• Tipo de dato del informe de selección: tipo de almacenamiento de los datos del informe

• Zona de recepción del informe de selección: dirección de almacenamiento del informe de selección; su significado se detalla al final del capítulo, en «[direcciones de la zona de recepción del informe de selección](#选点报告接收区地址)»

• Radio de búsqueda (píxeles): radio de búsqueda

• Color del cursor: color del cursor

• Notificación:

• Señal:

Nivel: con la selección activada, al seleccionar un punto del gráfico dibujado se activa esta opción y el bit de notificación pasa al estado indicado. Debe reiniciarse manualmente para poder detectar las notificaciones siguientes

Impulso: con la selección activada, al seleccionar un punto del gráfico dibujado se activa esta opción y el bit de notificación pasa a ON y se reinicia automáticamente

Bit de notificación: estado y dirección notificados al activarse la función

<span id="路径定义区地址说明"></span>**Direcciones de la zona de definición de la trayectoria:**

Zona de definición de la trayectoria: contiene los parámetros de dibujo con el formato siguiente. Ejemplo con la dirección LW0; significado de los datos:

|                     |                                                             |
|---------------------|-------------------------------------------------------------|
| Número de palabra         | Descripción                                                |
| LW0                 | Número de elementos de la trayectoria                     |
| LW1~LW8             | Información del primer elemento de la trayectoria  |
| LW9~LW16            | Información del segundo elemento de la trayectoria |
| ...                 | ...                                                         |
| LW（8n-7）~LW（8n） | Elemento n de la trayectoria                      |

Índice de elementos: [punto](#点), [línea](#线), [arco](#圆弧), [círculo](#圆), [espesor](#厚度), [color](#颜色)

<span id="点"></span>Punto:

|         |           |                       |
|---------|-----------|-----------------------|
| Palabra    | Nombre | Descripción              |
| LW1     | type      | Código del punto: 0   |
| LW2     | color     | [color](#颜色)        |
| LW3     | x         | Coordenada X del punto |
| LW4     | y         | Coordenada Y del punto |
| LW5~LW8 | (reservado)    | Por ahora 0           |

<span id="线"></span>Línea:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Palabra</p></td>
<td><p>Nombre</p></td>
<td><p>Descripción</p></td>
</tr>
<tr class="even">
<td><p>LW1</p></td>
<td><p>type</p></td>
<td><p>Código de la línea: 1</p></td>
</tr>
<tr class="odd">
<td><p>LW2</p></td>
<td><p>color</p></td>
<td><p><a href="#颜色">color</a></p></td>
</tr>
<tr class="even">
<td><p>LW3</p></td>
<td><p>X1</p></td>
<td><p>Coordenada X del punto inicial</p></td>
</tr>
<tr class="odd">
<td><p>LW4</p></td>
<td><p>Y1</p></td>
<td><p>Coordenada Y del punto inicial</p></td>
</tr>
<tr class="even">
<td><p>LW5</p></td>
<td><p>X2</p></td>
<td><p>Coordenada X del punto final</p></td>
</tr>
<tr class="odd">
<td><p>LW6</p></td>
<td><p>Y2</p></td>
<td><p>Coordenada Y del punto final</p></td>
</tr>
<tr class="even">
<td><p>LW7</p></td>
<td><p>style</p></td>
<td><p>Tipo de estilo:</p>
<p>0: no se muestra</p>
<p>1: <img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> línea continua</p>
<p>2: <img src="../../../configuration-guide/new_add_control/path-display.files/image004.jpg" width="40" alt="ScreenShot00232.jpg" /> línea discontinua</p>
<p>3: <img src="../../../configuration-guide/new_add_control/path-display.files/image005.jpg" width="40" alt="ScreenShot00234.jpg" /> línea de puntos</p>
<p>4: <img src="../../../configuration-guide/new_add_control/path-display.files/image006.jpg" width="40" alt="ScreenShot00235.jpg" /> línea de trazo y punto</p>
<p>5: <img src="../../../configuration-guide/new_add_control/path-display.files/image007.jpg" width="40" alt="ScreenShot00236.jpg" /> línea de trazo y dos puntos</p>
<p>6 o más:<img src="../../../configuration-guide/new_add_control/path-display.files/image002.jpg" width="40" alt="ScreenShot00233.jpg" /> línea continua</p></td>
</tr>
<tr class="odd">
<td><p>LW8</p></td>
<td><p>(reservado)</p></td>
<td><p>Por ahora 0</p></td>
</tr>
</tbody>
</table>

Arco (se dibuja en sentido antihorario del punto inicial al final):

|      |           |                             |
|------|-----------|-----------------------------|
| Palabra | Nombre | Descripción                    |
| 0    | type      | Código del arco: 2           |
| 1    | color     | [color](#颜色)              |
| 2    | X         | Coordenada X del centro        |
| 3    | Y         | Coordenada Y del centro         |
| 4    | X1        | Coordenada X del punto inicial |
| 5    | Y1        | Coordenada Y del punto inicial |
| 6    | X2        | Coordenada X del punto final      |
| 7    | Y2        | Coordenada Y del punto final      |

Círculo:

|      |           |                      |
|------|-----------|----------------------|
| Palabra | Nombre | Descripción             |
| 0    | type      | Código del círculo: 3 |
| 1    | color     | [color](#颜色)       |
| 2    | X         | Coordenada X del centro |
| 3    | Y         | Coordenada Y del centro  |
| 4    | r         | Radio del círculo        |
| 5~7  | (reservado)    | Por ahora 0          |

<span id="厚度"></span>Espesor (afecta a los elementos siguientes hasta el próximo espesor):

|      |                      |                                 |
|------|----------------------|---------------------------------|
| Palabra | Nombre            | Descripción                        |
| 0    | type                 | Código del espesor: 8                |
| 1    | (reservado)               | Por ahora 0                     |
| 2    | Espesor | Espesor del trazo, en píxeles |
| 3~7  | (reservado)               | Por ahora 0                     |

<span id="颜色"></span>Valores de color habituales:

|              |                                   |
|--------------|-----------------------------------|
| Color        | Valor (hexadecimal) |
| negro        | 0x0000                            |
| azul         | 0x0010                            |
| verde        | 0x0400                            |
| cian         | 0x0410                            |
| rojo         | 0x8000                            |
| magenta      | 0x8010                            |
| marrón        | 0x8400                            |
| gris         | 0xc618                            |
| gris oscuro    | 0x8410                            |
| azul claro   | 0x001f                            |
| verde claro  | 0x07e0                            |
| azul pálido    | 0x07ff                            |
| rosa         | 0xf800                            |
| magenta pálido | 0xf81f                            |
| amarillo       | Oxffe0                            |
| blanco        | 0xffff                            |

<span id="选点报告接收区地址"></span>**Direcciones de la zona de recepción del informe de selección**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Número de palabra</p></td>
<td colspan="3"><p>Descripción</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="3"><p>Coordenada X del punto seleccionado</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="3"><p>Coordenada Y del punto seleccionado</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td colspan="3"><p>Número de orden del elemento en el que está el punto seleccionado</p></td>
</tr>
<tr class="odd">
<td rowspan="3"><p>3</p></td>
<td colspan="2"><p>Valor</p></td>
<td><p>Descripción</p></td>
</tr>
<tr class="even">
<td><p>0</p></td>
<td colspan="2"><p>Punto: el punto</p>
<p>Línea: punto inicial de la línea</p>
<p>Círculo: centro del círculo</p>
<p>Arco: punto inicial del arco</p></td>
</tr>
<tr class="odd">
<td><p>1</p></td>
<td colspan="2"><p>Línea: punto final de la línea</p>
<p>Arco: punto final del arco</p></td>
</tr>
<tr class="even" height="0">
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>
