# Control por PLC

El control por PLC permite cambiar de pantalla, cambiar el nivel de usuario, cambiar de receta y escribir recetas desde el PLC. Haga doble clic en «Control por PLC» en el gestor de proyecto; se abre el cuadro de diálogo de la figura 7-8:

Figura 7-8      Cuadro de diálogo Control por PLC

• Cambiar receta: el HMI cambia de receta según el valor de la dirección.

• Escribir receta: el HMI controla la escritura de la receta según el valor de la dirección.

• Nivel de usuario actual: el HMI ajusta el nivel de usuario actual según el valor de esta dirección.

• Cambio de pantalla por dirección de palabra: el HMI cambia de pantalla según el valor de esta dirección de palabra; si vale n, pasa a la pantalla n.

• Cambio de pantalla por dirección de bit: haga doble clic en la línea «Nuevo»; se abre el cuadro de diálogo de la figura 7-9:

Nuevo control por bit:

<img src="../../setting/plc-control.files/image004.jpg" width="458" />

Nuevo control por palabra

<img src="../../setting/plc-control.files/image006.jpg" width="497" />

Pantalla: el control por palabra del PLC solo cambia entre pantallas

Ventana: el control por palabra del PLC solo cambia entre ventanas

Pantalla / ventana: el control por palabra del PLC cambia entre pantallas y ventanas

<img src="../../setting/plc-control.files/image005.jpg" width="130" />

Nota: al cambiar de pantalla desde el PLC, el primer valor leído no provoca el cambio. Solo actúa cuando el valor del registro del PLC es distinto del primer valor leído.
