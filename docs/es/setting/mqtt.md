# Servidor

• **Página «General»**

<img src="../../setting/mqtt.files/server-general.png" width="706" />

- IP (nombre de dominio)

IP del servidor MQTT

- Puerto

Número de puerto del servidor MQTT

- ID de cliente

ID de cliente; se admiten ciertos caracteres especiales

- Nombre de usuario

Nombre de usuario (requiere la autenticación activada)

- Contraseña

Contraseña del usuario (requiere la autenticación activada)

- Duración de la prueba de conexión

Si transcurrido este tiempo el servidor MQTT no ha recibido el mensaje de prueba del HMI, considera que el HMI está desconectado.

• **Página «Dirección»**

<img src="../../setting/mqtt.files/server-addr.png" width="706" />

- Dirección de estado

Define un grupo de direcciones de palabra para comprobar el estado de la conexión.

**\[Dirección de estado\] (indicación de estado)**

Valor 0: conexión con el servidor detenida.

Valor 1: desconectado del servidor.

Valor 2: conectado al servidor.

**■   \[Dirección de estado + 1\] (indicación de error)**

|                      |                                                                                                                                                                                                                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Valor** | **Descripción**                                                                                                                                                                                                                                                                             |
| 0                    | Operación completada correctamente                                                                                                                                                                                                                                                        |
| -1                   | Error en la operación del cliente MQTT                                                                                                                                                                                                                                                                |
| -2                   | Errores de persistencia                                                                                                                                                                                                                                                                           |
| -3                   | Cliente desconectado                                                                                                                                                                                                                                                                         |
| -4                   | Se ha alcanzado el número máximo de mensajes simultáneos                                                                                                                                                                                                         |
| -5                   | Cadena UTF-8 no válida detectada                                                                                                                                                                                                                                                               |
| -6                   | Se ha pasado un parámetro vacío no válido                                                                                                                                                                                                                                                     |
| -7                   | El asunto se ha truncado (contiene caracteres NULL); use la longitud del asunto para acceder al asunto completo                                                                                                                                              |
| -8                   | El parámetro de estructura no tiene el identificador (eye catcher) ni el número de versión correctos                                                                                                                                                                                                            |
| -9                   | El parámetro qos no es 0, 1 ni 2                                                                                                                                                                                                                                                          |
| -10                  | Los 65535 msgids MQTT están en uso                                                                                                                                                                                                                                                            |
| -11                  | La solicitud está incompleta y se descarta                                                                                                                                                                                                                                          |
| -12                  | No se pueden almacenar más mensajes                                                                                                                                                                                                                                                                 |
| -13                  | Intento de usar la versión no SSL de la biblioteca para una conexión SSL                                                                                                                                                                                                                         |
| -14                  | El prefijo de protocolo en serverURI debe ser: tcp:// o mqtt:// (TCP sin cifrar), ssl:// o mqtts:// (SSL/TLS cifrado), ws:// (WebSockets no seguros) o wss:// (WebSockets seguros). Los prefijos TLS (ssl, mqtts, wss) solo son válidos si se enlaza la versión TLS de la biblioteca |
| -15                  | No use otras versiones de la opción MQTT                                                                                                                                                                                                                                                |
| -16                  | La llamada no se aplica a la versión MQTT del cliente                                                                                                                                                                                                                                   |
| -17                  | La longitud del asunto Will es cero                                                                                                                                                                                                                                                                 |
| -18                  | Orden de conexión o desconexión ignorada porque ya hay una al principio de la cola. Use las callbacks onSuccess/onFailure para esperar a que termine la orden anterior                                                    |
| -19                  | maxBufferedMessages en las opciones de conexión debe ser &gt;=0                                                                                                                                                                                                                                      |

- Dirección de control

**Tipo de dato del registro: entero de 16 bits.**

Si el valor es menor o igual que 0, se desconecta del servidor MQTT.

Si el valor es mayor que 0, se mantiene la conexión con el servidor MQTT.
