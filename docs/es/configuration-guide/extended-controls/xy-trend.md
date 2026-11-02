# Gráfico de tendencia XY

**Presentación del gráfico de tendencia XY:**

Muestra de forma dinámica y continua los valores de las variables.

Dibuja varias curvas de referencia, con los valores de dos registros consecutivos como coordenadas horizontal y vertical, para observar con precisión e intuición su relación.

Se pueden mostrar hasta 8 polilíneas (curvas).

El gráfico de tendencia XY se añade y configura como el gráfico de tendencia; véase la página «Gráfico de tendencia». Icono:<img src="../../../configuration-guide/extended-controls/xy-trend.files/image002.jpg" width="36" />

Abra el cuadro de propiedades de la tendencia XY; véanse los ajustes del «Gráfico de tendencia». Diferencia: en el gráfico de tendencia cada curva representa el valor de direcciones consecutivas a partir de la dirección de escritura; en el gráfico XY, cada curva representa los valores de dos direcciones consecutivas.

**Uso del gráfico de tendencia XY:**

Color: color de la línea de detección (línea de referencia).

Dirección de detección: el valor de la línea de detección actual se escribe en esta dirección.

Por ejemplo, con el tipo de dato de 16 bits y 4 grupos de datos, si la dirección introducida es LW3, se leen 8 valores consecutivos:

LW3: curva 1, valor del eje X

LW4: curva 1, valor del eje Y

LW5: curva 2, valor del eje X

LW6: curva 2, valor del eje Y

LW7: curva 3, valor del eje X

LW8: curva 3, valor del eje Y

LW9: curva 4, valor del eje X

LW10: curva 4, valor del eje Y

Las direcciones leídas son LW3-LW10, es decir, 8 direcciones. Así, con datos de 16 bits y N grupos, se leen 2 \* N direcciones consecutivas según las reglas de direccionamiento de cada PLC.

Con el tipo de dato de 32 bits y 3 grupos, si la dirección introducida es LW3, se leen los valores siguientes:

LW3: curva 1, valor del eje X

LW5: curva 1, valor del eje Y

LW7: curva 2, valor del eje X

LW9: curva 2, valor del eje Y

LW11: curva 3, valor del eje X

LW13: curva 3, valor del eje Y

Las direcciones leídas son LW3-LW14, es decir, 12 direcciones. Así, con datos de 32 bits y N grupos, se leen 2 \* N valores incrementando la dirección de 2 en 2 según las reglas de direccionamiento de cada PLC.
