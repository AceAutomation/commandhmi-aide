# Conexión de paso

Las pantallas táctiles admiten una conexión especial: un HMI remoto supervisa o controla un PLC u otro equipo a través del puerto serie de otro HMI conectado a ese equipo. Así, el equipo puede manejarse desde dos o más puestos. La conexión de paso es una función muy útil del HMI.

Antes de usar la conexión de paso conviene conocer estos términos:

• HMI local: el HMI conectado al PLC u otro equipo.

• HMI remoto: el HMI conectado al HMI local, que controla los equipos a través de la conexión de paso.

Para una conexión de paso, el HMI local necesita dos puertos serie. Los esquemas se muestran en las figuras 8-12 y 8-13:

Conexión de paso con dos HMI:

<img src="../../multpoint/penetrate.files/penetrate789.png" width="578" />

Figura 8-12    Esquema de conexión de paso con dos HMI

Conexión de paso con varios HMI:

<img src="../../multpoint/penetrate.files/penetrate913.png" width="792" />

Figura 8-13    Esquema de conexión de paso con varios HMI

HMI local: ajustes de software:

Haga doble clic en la conexión creada; se abre la ventana de propiedades del puerto de comunicación. Elija COM1 como puerto de conexión. Ejemplo con MITSUBISHI: el COM1 del HMI local está conectado a un PLC MITSUBISHI FX2N. Los parámetros de comunicación deben coincidir con los del PLC o equipo conectado. Véanse las figuras 8-14 y 8-15:

<img src="../../multpoint/penetrate.files/penetrate1423.png" width="589" />

Figura 8-14    Página «General» de las propiedades del puerto del HMI local

<img src="../../multpoint/penetrate.files/penetrate1500.png" width="587" />

Figura 8-15: Página COM1 de las propiedades del puerto del HMI local

Cree una nueva conexión, elija COM2 como puerto, no añada ningún protocolo en «Conexión» y ajuste las propiedades como sigue, con los mismos parámetros serie que el puerto 1. Recomendado: 9600, 8, None, 1. Elija «Puerto hacia HMI esclavo» (Connect Slave Screen Port) como propiedad de paso y ajuste el número de HMI según el caso. Véanse las figuras 8-16 y 8-17.

<img src="../../multpoint/penetrate.files/image001.jpg" width="598" alt="ScreenShot00093.jpg" />

Figura 8-16    Página «General» de las propiedades del puerto del HMI local

<img src="../../multpoint/penetrate.files/penetrate2042.png" width="589" />

Figura 8-17    Página «Parámetros» de las propiedades del puerto del HMI local

Deje los demás parámetros por defecto. El HMI local queda configurado.

HMI remoto: ajustes de software:

Haga doble clic en la conexión creada; se abre la ventana de propiedades del puerto de comunicación. Elija COM1 como puerto de conexión y «Remoto» (Remote) como ubicación del HMI, con los mismos parámetros de comunicación que en la página COM2 del HMI local (véase la figura 6 anterior), como en las figuras 8-18 y 8-19.

<img src="../../multpoint/penetrate.files/penetrate2646.png" width="589" />

Figura 8-18    Página «General» de las propiedades del puerto del HMI remoto

<img src="../../multpoint/penetrate.files/penetrate2724.png" width="588" />

Figura 8-19    Página «Parámetros» de las propiedades del puerto del HMI remoto

Deje los demás parámetros por defecto. El HMI remoto queda configurado.

<img src="../../multpoint/penetrate.files/penetrate2924.png" width="130" />

Nota: estos ajustes corresponden a la conexión de paso con dos HMI.

Nota: en la conexión de paso con varios HMI, el ajuste COM de los HMI remotos es igual al del HMI local.

Nota: como todos los datos pasan por el COM1 del HMI local, la comunicación es lenta en una conexión de paso con varios HMI.
