# HTTP

<img src="../../setting/lisanbaojing.files/image007.jpg" width="133" alt="lisanbaojing2414" /> Solo la pantalla remota admite esta función

![](../../setting/http.files/open.png)

Esta función permite configurar fácilmente los parámetros del servidor HTTP

Ø  Página «General»

<img src="../../setting/http.files/general.png" width="606" />

- Nombre

Nombre de la conexión

- URL

URL de destino de la solicitud HTTP

- Método

Método de la solicitud HTTP: GET o POST

- Codificación

Formato de codificación

- Cabecera de la solicitud

Cabecera de la solicitud HTTP

- Tiempo de espera

Tiempo de respuesta HTTP

- Formatos

JSON (general) o JSON (avanzado), [igual que en 【MQTT】](mqtttheme.md#anchor-name)

- Modos de transmisión

automático y por disparo de bit

Ø  Página «Dirección» (JSON general)

Disponible cuando el formato elegido en la página \[General\] es \[JSON general\].

Añade un valor de tipo bit o palabra, fijo o leído de una dirección indicada. [Véase 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Página «Enviar JSON» (JSON avanzado)

Disponible cuando el formato elegido en la página \[General\] es \[JSON avanzado\].
<img src="../../setting/http.files/sendjson.png" width="606" />

Define los datos enviados. Las direcciones admiten una estructura en árbol con elementos, arrays, etc.; la marca de tiempo y los nombres de datos son personalizables. [Véase 【MQTT】](mqtttheme.md#anchor-name1)

Ø  Página «Recibir JSON»

<img src="../../setting/http.files/receivejson.png" width="606" />

Define los datos recibidos. Las direcciones admiten una estructura en árbol con elementos, arrays, etc.; la marca de tiempo y los nombres de datos son personalizables. Véase [【Enviar JSON】](#anchor-name)

Ø  Página «Seguridad»

Véase la página \[Seguridad\] de [\[MQTT\].](mqtttheme.md#anchor-name2)
