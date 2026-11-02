# Reloj

El ajuste del reloj incluye tres funciones: cargar la hora del sistema en el HMI, escribir la hora en el PLC y sincronizarla con el PLC.

Haga doble clic en «Reloj» en el gestor de proyecto para abrir sus propiedades.

<img src="../../setting/clock.files/image004.jpg" width="388" />

<img src="../../setting/clock.files/image005.jpg" width="388" />

Figura 7-11 Cuadro de diálogo Reloj

Cargar el reloj del sistema en el HMI: indica si la hora del sistema se carga en el HMI.

• Escribir hora/fecha en el PLC:

• El tipo de dato y la longitud son valores por defecto.

• Hora: año-mes-día-hora-minuto-segundo-día de la semana. Véase LW 60000~LW 60006 en las direcciones de registros. El día de la semana de la hora del sistema no puede modificarse.

Dirección de escritura: la hora del sistema se escribe en esta dirección del PLC.

• Modo de activación:

Periódico: escribe la hora del sistema en la dirección del PLC con el intervalo definido.

Disparo: escribe la hora del sistema en la dirección del PLC cuando la dirección de disparo vale 1.

Reinicio automático: pone automáticamente a 0 la dirección de disparo cuando vale 1.

**Sincronización con la hora del PLC:**

El tipo de dato y la longitud son valores por defecto.

 Hora: año-mes-día-hora-minuto-segundo-día de la semana. Véase LW 60000~LW 60006 en las direcciones de registros. El día de la semana de la hora del sistema no puede modificarse.

• Dirección de lectura: se lee la información de esta dirección del PLC.

• Modo de activación:

Periódico: escribe la hora del sistema en la dirección del PLC con el intervalo definido.

Disparo: la hora del sistema se sincroniza con el PLC cuando la dirección de disparo vale 1.

Reinicio automático: pone automáticamente a 0 la dirección de disparo cuando vale 1.
