# Topic

Ø  Añadir un topic de publicación

• Página «General»

![](../../setting/mqtttheme.files/addpublish.png)

- Nombre

Nombre del proyecto del topic MQTT

- Topic

Topic con el que el servidor MQTT recibe el mensaje enviado

- Formato

\[JSON (general)\]: datos en formato JSON con estructura de lista.

\[JSON (avanzado)\]: formato JSON con estructura de árbol personalizable.

- Modo de envío

**■  automático**

Por cambio de valor: cuando cambia el contenido de la dirección de monitorización, se transmite automáticamente.

Periódico: el contenido de la dirección de monitorización se transmite periódicamente.

**■  disparo por bit**

El contenido se transmite cuando se activa la dirección de bit indicada.

• Dirección (JSON general)

Disponible cuando el formato elegido en la página \[General\] es \[JSON general\].
<img src="../../setting/mqtttheme.files/addgeneraladdr.png" width="606" />

Añade un valor de tipo bit o palabra, fijo o leído de una dirección indicada.

• Dirección (JSON avanzado)

Disponible cuando el formato elegido en la página \[General\] es \[JSON avanzado\].
<img src="../../setting/mqtttheme.files/addextendaddr.png" width="606" />

Las direcciones admiten una estructura en árbol con elementos, arrays, etc.; la marca de tiempo y los nombres de datos son personalizables.

- Elemento

Añade un elemento de datos. Un elemento puede contener varios formatos de datos, cada uno con su nombre y su valor.

Los datos del elemento van entre llaves { }.

- Array

Añade un array de datos. Un array puede contener varios formatos de datos, pero tiene un solo nombre.

Los datos van entre corchetes \[ \].

- Valor

Añade un valor, una cadena o una marca de tiempo. El valor o la cadena pueden ser fijos o leerse de una dirección indicada.

- Plantilla

Convierte un texto JSON editado por el usuario en estructura de árbol

- Vista previa

Convierte la estructura de árbol actual en texto JSON

• Página «Seguridad»

Si se activa, surte efecto cuando la dirección de bit definida cumple la condición de disparo.
<img src="../../setting/mqtttheme.files/publishsecurity.png" width="606" />

Ø  Añadir un topic de suscripción

• Página «General»

<img src="../../setting/mqtttheme.files/addsubscribe.png" width="606" />

- Nombre

Nombre del proyecto del topic MQTT

- Topic

Topic suscrito en el servidor MQTT

- Formato

[igual que en 【Publicar】](#anchor-name)

- Modo de funcionamiento

■  automático

automáticamente.

■  Manual

Se ejecuta al activar manualmente la dirección indicada.

• Página «Dirección»

[Igual que en 【Publicar】](#anchor-name)

• Página «Seguridad»

[Igual que en 【Publicar】](#anchor-name)
