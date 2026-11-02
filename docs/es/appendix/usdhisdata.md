# Exportar datos mediante memoria USB

Los HMI de la serie HM permiten exportar datos históricos, recetas, alarmas históricas y capturas de pantalla a una memoria USB.

Como CommandHMI admite varios grupos de datos históricos, para exportarlos hay que indicar el número de grupo. LW60408 contiene el número del grupo seleccionado. Por ejemplo: si LW60408 vale 1, la importación y exportación por memoria USB afecta únicamente al grupo de datos históricos 0.

Nota: si el valor introducido supera el número máximo de grupos menos 1, la función no actúa.

**Cómo exportar datos históricos a una memoria USB**

1\. Inserte la memoria USB

2\. Indique en el registro LW60408 el número de grupo de datos históricos a importar/exportar.

3\. Ponga LB60127 a ON: el HMI copia el archivo del grupo de datos históricos en la memoria USB con el nombre hisdatai.csv; hisdata1.csv si el número de grupo es 1.

Ponga LB60128 a ON y el HMI copia el archivo del grupo de datos históricos en la memoria USB; para importar el grupo 1, el archivo debe llamarse hisdata1.csv.

Estos bits de disparo vuelven automáticamente a OFF al terminar la exportación

Para exportar datos locales se usan los registros LW: LW60359-LW60429

**Cómo exportar recetas**

Como CommandHMI admite varios grupos de recetas, para exportarlas hay que ajustar LW61143.

1\. Inserte la memoria USB.

2\. Indique el número de grupo en LW61143.

3\. Ponga LB60163 a ON: el HMI copia el archivo de recetas del grupo en la memoria USB

4\. Estos bits de disparo vuelven automáticamente a OFF al terminar la exportación

Nota: los datos históricos exportados no pueden abrirse directamente en el ordenador; hace falta la herramienta de conversión SK_SQL_CSV.exe, <img src="../../appendix/usdhisdata.files/image002.jpg" width="86" />que se encuentra en el directorio raíz del software de configuración HM.

Esta herramienta convierte el archivo exportado en un archivo CSV que puede abrirse directamente. Haga doble clic para abrir la herramienta.

Progreso: avance de la conversión.

Nombre de archivo: elija el archivo a convertir.

Elija datos históricos o alarmas según corresponda. La codificación por defecto es ANSI y no puede cambiarse. Haga clic en «Generar CSV»; la conversión termina cuando la barra de progreso llega al 100 %.

**Cómo obtener capturas de pantalla en una memoria USB**

1\. Inserte la memoria USB

2\. En la configuración, cree un botón de función -&gt; Captura de pantalla y elija «Exportar a memoria USB»

3\. Al tocar este botón de función, el HMI guarda la pantalla actual en la memoria correspondiente

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />

Nota:

 • No retire la memoria USB durante la exportación;

• Mantenga la alimentación encendida durante la exportación;

• Compruebe que la memoria USB tiene espacio suficiente.

<img src="../../appendix/usdhisdata.files/image004.gif" width="595" />
