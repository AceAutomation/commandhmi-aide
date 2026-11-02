# Transferencia de datos

Sirve para transferir datos entre el PLC y el HMI o entre dos PLC. Haga clic en «Transferencia de datos» en el gestor de proyecto para ver la lista de transferencias.

<img src="../../../configuration-guide/extended-controls/transmission.files/image005.jpg" width="564" />

Figura 7-36

La lista muestra el detalle de todas las transferencias actuales. El usuario puede crearlas, eliminarlas y modificarlas. El software CommandHMI admite hasta 512 transferencias de datos.

Para crear o modificar una transferencia hay que abrir su página de propiedades:

<img src="../../../configuration-guide/extended-controls/transmission.files/image006.jpg" width="339" />

Figura 7-37

**1. Atributos**

Periódico / disparo: modo de activación de la transferencia.

Periódico: la transferencia se realiza con el intervalo definido.

Disparo: la transferencia la controla una dirección; se ejecuta cuando la dirección vale 1.

Reinicio automático: cuando la dirección de disparo vale 1, se pone automáticamente a 0.

Tipo de dirección: tipo de dirección transferida: bit / palabra / doble palabra.

Palabras / bits: longitud de los datos a transferir, de 1 a 64.

**2. Dirección**

Dirección de origen: dirección de origen de los datos, <span id="OLE_LINK497"></span><span id="OLE_LINK498"></span>del mismo tipo que el definido en «Atributos».

Dirección de destino: dirección de destino de los datos, del mismo tipo que el definido en «Atributos».

<img src="../../../configuration-guide/extended-controls/transmission.files/image004.jpg" width="130" />

Las direcciones de origen y destino no pueden estar en el mismo PLC.
