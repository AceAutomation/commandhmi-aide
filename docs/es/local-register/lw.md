# LW

LW

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Dirección</th>
<th>Descripción</th>
<th>Notas</th>
<th>Lectura/escritura</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>59010~59057</td>
<td>En modo extendido, bloquea la comunicación con la estación indicada. Estaciones 0~255,<br />
cada dirección corresponde a 16 números de estación: 59010 corresponde a las estaciones 0~15, etc. Si el bit X vale 1, se permite la comunicación con la estación X; si vale 0,<br />
la comunicación con la estación X está desactivada.</td>
<td>COM1: 59010~59025<br />
COM2: 59026~59041<br />
COM3: 59106~59121<br />
Ethernet: 59042~59057</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>59058~59105</td>
<td>Indicación del estado de comunicación por estación, estaciones 0~255.<br />
cada dirección corresponde a 16 números de estación: 59058 corresponde a las estaciones 0~15, etc. Si el bit X vale 1,<br />
la comunicación con esa estación es anómala; si vale 0, es normal.</td>
<td>COM1: 59058~59073<br />
COM2: 59074~59089<br />
COM3: 59154~59169<br />
Ethernet: 59090~59105</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60000</td>
<td>Hora local: segundos</td>
<td>Código BCD, rango válido 0-59</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60001</td>
<td>Hora local</td>
<td>Código BCD, rango válido 0-59</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60002</td>
<td>Hora local</td>
<td>Código BCD, rango válido 0-23</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60003</td>
<td>Hora local: día</td>
<td>Código BCD, rango válido 1-31</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60004</td>
<td>Hora local: mes</td>
<td>Código BCD, rango válido 1-12</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60005</td>
<td>Hora local: año</td>
<td>Código BCD, rango válido 0-9999</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60006</td>
<td>Hora local: día de la semana</td>
<td>Código BCD, rango válido 1-7</td>
<td>R</td>
</tr>
<tr class="even">
<td>60007</td>
<td>Tiempo de funcionamiento</td>
<td>Tiempo de funcionamiento del sistema en horas</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60008</td>
<td>Tiempo de funcionamiento</td>
<td>Tiempo transcurrido desde el arranque en minutos</td>
<td>R</td>
</tr>
<tr class="even">
<td>60009</td>
<td>Tiempo de funcionamiento en segundos</td>
<td>Tiempo transcurrido desde el arranque en segundos</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60010</td>
<td>Número de la pantalla/ventana actual</td>
<td>Número de la pantalla mostrada</td>
<td>R</td>
</tr>
<tr class="even">
<td>60012</td>
<td>Idioma actual</td>
<td>Número del idioma correspondiente</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60013</td>
<td>Límite superior de la entrada numérica</td>
<td>Al abrir el teclado personalizado, se muestra en ASCII el límite superior permitido</td>
<td>R</td>
</tr>
<tr class="even">
<td>60023</td>
<td>Límite inferior de la entrada numérica</td>
<td>Al abrir el teclado personalizado, se muestra en ASCII el límite inferior permitido</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60033</td>
<td>Datos de entrada mostrados en el teclado</td>
<td>Datos de entrada mostrados en el teclado (caracteres tecleados), visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60065</td>
<td>Usuario conectado</td>
<td>Número del usuario actual</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60066</td>
<td>Contraseña del usuario conectado</td>
<td>Muestra la contraseña del usuario actual, 16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60074</td>
<td>Nombre del usuario conectado</td>
<td>Muestra el nombre del usuario actual, 32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60090</td>
<td>Usuario 1 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="even">
<td>60091</td>
<td>Usuario 2 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60092</td>
<td>Usuario 3 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="even">
<td>60093</td>
<td>Usuario 4 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60094</td>
<td>Usuario 5 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="even">
<td>60095</td>
<td>Usuario 6 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60096</td>
<td>Usuario 7 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="even">
<td>60097</td>
<td>Usuario 8 activado</td>
<td>0 - desactivado, 1 - activado</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60098</td>
<td>Nombre del usuario 1</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60114</td>
<td>Nombre del usuario 2</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60130</td>
<td>Nombre del usuario 3</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60146</td>
<td>Nombre del usuario 4</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60162</td>
<td>Nombre del usuario 5</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60178</td>
<td>Nombre del usuario 6</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60194</td>
<td>Nombre del usuario 7</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60210</td>
<td>Nombre del usuario 8</td>
<td>32 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60226</td>
<td>Contraseña del usuario 1</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60234</td>
<td>Contraseña del usuario 2</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60242</td>
<td>Contraseña del usuario 3</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60250</td>
<td>Contraseña del usuario 4</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60258</td>
<td>Contraseña del usuario 5</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60266</td>
<td>Contraseña del usuario 6</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60274</td>
<td>Contraseña del usuario 7</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="even">
<td>60282</td>
<td>Contraseña del usuario 8</td>
<td>16 caracteres, visualización ASCII</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60290</td>
<td>Tiempo del salvapantallas</td>
<td>Muestra el tiempo de salvapantallas definido en el proyecto, rango 0~60</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60291</td>
<td>Periodo de parpadeo de las lámparas</td>
<td>Periodo de parpadeo de los objetos lámpara, mínimo 0,1, en s</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60292</td>
<td>Posición X al tocar</td>
<td>Coordenada X del punto tocado</td>
<td>R</td>
</tr>
<tr class="even">
<td>60293</td>
<td>Posición Y al tocar</td>
<td>Coordenada Y del punto tocado</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60294</td>
<td>Posición X al soltar</td>
<td>Coordenada X al soltar</td>
<td>R</td>
</tr>
<tr class="even">
<td>60295</td>
<td>Posición Y al soltar</td>
<td>Coordenada Y al soltar</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60296</td>
<td>Estado táctil</td>
<td>1-tocado, 0-soltado</td>
<td>R</td>
</tr>
<tr class="even">
<td>60297</td>
<td>Paridad de COM1</td>
<td>Parámetro de comunicación, paridad: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60298</td>
<td>Velocidad de COM1</td>
<td>Parámetro de comunicación, velocidad: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60299</td>
<td>Bits de parada de COM1</td>
<td>Parámetro de comunicación, bits de parada: 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60300</td>
<td>Longitud de datos de COM1</td>
<td>Parámetro de comunicación, longitud de datos: 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60301</td>
<td>Dirección HMI de COM1</td>
<td>Parámetro de comunicación, dirección del HMI</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60302</td>
<td>Dirección PLC de COM1</td>
<td>Parámetro de comunicación, dirección del PLC</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60303</td>
<td>COM1: intervalo de direcciones continuas del PLC</td>
<td>Longitud máxima de direcciones continuas leídas en una comunicación</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60304</td>
<td>COM1: tiempo de comunicación</td>
<td>Retardo de comunicación</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60305</td>
<td>COM1: reintentos</td>
<td>Número de reintentos en caso de fallo de comunicación</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60306</td>
<td>COM1: modo de direccionamiento</td>
<td>Modo de direccionamiento: 0-estándar, 1-extendido</td>
<td>R</td>
</tr>
<tr class="even">
<td>60307</td>
<td>COM1: tiempo de espera de la comunicación</td>
<td>Tiempo de espera de la comunicación en ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60308</td>
<td>COM1: tiempo de espera actual de la comunicación</td>
<td>Tiempo de espera actual de la comunicación en ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60309</td>
<td>COM1: ubicación del HMI</td>
<td>0-local 1-remoto</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60312</td>
<td>Paridad de COM2</td>
<td>Parámetro de comunicación, paridad: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60313</td>
<td>Velocidad de COM2</td>
<td>Parámetro de comunicación, velocidad: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60314</td>
<td>Bits de parada de COM2</td>
<td>Parámetro de comunicación, bits de parada: 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60315</td>
<td>Longitud de datos de COM2</td>
<td>Parámetro de comunicación, longitud de datos: 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60316</td>
<td>Dirección HMI de COM2</td>
<td>Parámetro de comunicación, dirección del HMI</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60317</td>
<td>Dirección PLC de COM2</td>
<td>Parámetro de comunicación, dirección del PLC</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60318</td>
<td>COM2: intervalo de direcciones continuas del PLC</td>
<td>Longitud máxima de direcciones continuas leídas en una comunicación</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60319</td>
<td>COM2: tiempo de comunicación</td>
<td>Retardo de comunicación</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60320</td>
<td>COM2: reintentos</td>
<td>Número de reintentos en caso de fallo de comunicación</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60321</td>
<td>COM2: modo de direccionamiento</td>
<td>Modo de direccionamiento: 0-estándar, 1-extendido</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60322</td>
<td>COM2: tiempo de espera de la comunicación</td>
<td>Tiempo de espera de la comunicación en ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60323</td>
<td>COM2: tiempo de espera actual de la comunicación</td>
<td>Tiempo de espera actual de la comunicación en ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60324</td>
<td>COM2: ubicación del HMI</td>
<td>0-local, 1-remoto</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61270</td>
<td>Paridad de COM3</td>
<td>Parámetro de comunicación, paridad: 0-NONE, 1-EVEN, 2-ODD</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61271</td>
<td>Velocidad de COM3</td>
<td>Parámetro de comunicación, velocidad: 0-1200, 1-2400, 2-4800, 3-9600, 4-19200, 5-38400, 6-57600, 7-115200</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61272</td>
<td>Bits de parada de COM3</td>
<td>Parámetro de comunicación, bits de parada: 0-1 bit, 1-2 bits</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61273</td>
<td>Longitud de datos de COM3</td>
<td>Parámetro de comunicación, longitud de datos: 0-7 bits, 1-8 bits</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61274</td>
<td>Dirección HMI de COM3</td>
<td>Parámetro de comunicación, dirección del HMI</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61275</td>
<td>Dirección PLC de COM3</td>
<td>Parámetro de comunicación, dirección del PLC</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61276</td>
<td>COM3: intervalo de direcciones continuas del PLC</td>
<td>Longitud máxima de direcciones continuas leídas en una comunicación</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61277</td>
<td>COM3: tiempo de comunicación</td>
<td>Retardo de comunicación</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61278</td>
<td>COM3: reintentos</td>
<td>Número de reintentos en caso de fallo de comunicación</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61279</td>
<td>COM3: modo de direccionamiento</td>
<td>Modo de direccionamiento: 0-estándar, 1-extendido</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61280</td>
<td>COM3: tiempo de espera de la comunicación</td>
<td>Tiempo de espera de la comunicación en ms</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61281</td>
<td>COM3: tiempo de espera actual de la comunicación</td>
<td>Tiempo de espera actual de la comunicación en ms</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61282</td>
<td>COM3: ubicación del HMI</td>
<td>0-local, 1-remoto</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60327</td>
<td>Número de alarmas históricas</td>
<td>Número total de alarmas históricas registradas</td>
<td>L/doble palabra</td>
</tr>
<tr class="even">
<td>60329</td>
<td>Número de datos históricos</td>
<td>Número total de registros históricos</td>
<td>L/doble palabra</td>
</tr>
<tr class="odd">
<td>60333</td>
<td>Idioma del teclado</td>
<td>1-teclado chino, 0-teclado inglés, para el teclado estándar</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60334</td>
<td>Uso de la CPU</td>
<td>Uso de la CPU del sistema</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60335</td>
<td>Brillo actual de la retroiluminación</td>
<td>Brillo actual de la retroiluminación (140~450)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60337</td>
<td>Fecha de creación del proyecto: año</td>
<td>Año de creación del archivo de proyecto actual</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60338</td>
<td>Fecha de creación del proyecto: mes</td>
<td>Mes de creación del archivo de proyecto actual</td>
<td>R</td>
</tr>
<tr class="even">
<td>60339</td>
<td>Fecha de creación del proyecto: día</td>
<td>Día de creación del archivo de proyecto actual</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60340</td>
<td>Idioma de usuario actual</td>
<td>Define el idioma actual</td>
<td>W</td>
</tr>
<tr class="even">
<td>60359</td>
<td>Con 1, las alarmas históricas del rango de números indicado se copian a la memoria USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60361</td>
<td>Con 1, las alarmas históricas del rango de tiempo indicado se copian a la memoria USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60363</td>
<td>Exportación de alarmas históricas: número inicial</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60365</td>
<td>Exportación de alarmas históricas: número final</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60367</td>
<td>Exportación de alarmas históricas: hora inicial</td>
<td>Longitud 6 palabras: año, mes, día, hora, minuto y segundo.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60373</td>
<td>Exportación de alarmas históricas: hora final</td>
<td>Longitud 6 palabras: año, mes, día, hora, minuto y segundo.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60379</td>
<td>Nombre de archivo al exportar alarmas históricas a la memoria USB</td>
<td>Longitud 22 caracteres</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60408</td>
<td>Dirección de control del grupo actual de datos históricos</td>
<td>Define el grupo actual de datos históricos</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60409</td>
<td>Con 1, los datos históricos del rango de números indicado se copian a la memoria USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60411</td>
<td>Con 1, los datos históricos del rango de tiempo indicado se copian a la memoria USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60413</td>
<td>Exportación de datos históricos: número inicial</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60415</td>
<td>Exportación de datos históricos: número final</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60417</td>
<td>Exportación de datos históricos: hora inicial</td>
<td>Longitud 6 palabras: año, mes, día, hora, minuto y segundo.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60423</td>
<td>Exportación de datos históricos: hora final</td>
<td>Longitud 6 palabras: año, mes, día, hora, minuto y segundo.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60429</td>
<td>Nombre de archivo al exportar datos históricos a la memoria USB</td>
<td>Longitud 24 caracteres</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60441</td>
<td>Búfer para cambiar la contraseña del usuario 1</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60449</td>
<td>Activar el cambio de contraseña del usuario 1</td>
<td>Con 1, la contraseña del usuario 1 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60451</td>
<td>Búfer para cambiar la contraseña del usuario 2</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60459</td>
<td>Activar el cambio de contraseña del usuario 2</td>
<td>Con 1, la contraseña del usuario 2 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60461</td>
<td>Búfer para cambiar la contraseña del usuario 3</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60469</td>
<td>Activar el cambio de contraseña del usuario 3</td>
<td>Con 1, la contraseña del usuario 3 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60471</td>
<td>Búfer para cambiar la contraseña del usuario 4</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60479</td>
<td>Activar el cambio de contraseña del usuario 4</td>
<td>Con 1, la contraseña del usuario 4 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60481</td>
<td>Búfer para cambiar la contraseña del usuario 5</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60489</td>
<td>Activar el cambio de contraseña del usuario 5</td>
<td>Con 1, la contraseña del usuario 5 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60491</td>
<td>Búfer para cambiar la contraseña del usuario 6</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60499</td>
<td>Activar el cambio de contraseña del usuario 6</td>
<td>Con 1, la contraseña del usuario 6 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60501</td>
<td>Búfer para cambiar la contraseña del usuario 7</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60509</td>
<td>Activar el cambio de contraseña del usuario 7</td>
<td>Con 1, la contraseña del usuario 7 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60511</td>
<td>Búfer para cambiar la contraseña del usuario 8</td>
<td>Longitud 16 caracteres, visualización ASCII</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60519</td>
<td>Activar el cambio de contraseña del usuario 8</td>
<td>Con 1, la contraseña del usuario 8 se sustituye por la del búfer; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60520</td>
<td>Modelo de HMI</td>
<td>40 caracteres</td>
<td>R</td>
</tr>
<tr class="even">
<td>60540</td>
<td>Versión del bootloader</td>
<td>40 caracteres</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60560</td>
<td>Versión del sistema operativo</td>
<td>40 caracteres</td>
<td>R</td>
</tr>
<tr class="even">
<td>60580</td>
<td>Versión del software</td>
<td>40 caracteres</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60600</td>
<td>Activar el registro de operaciones</td>
<td>Con 1 se registran las operaciones</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60601</td>
<td>Número de entradas del registro</td>
<td>Muestra el número actual de entradas del registro</td>
<td>R</td>
</tr>
<tr class="odd">
<td>60602</td>
<td>Activar captura de pantalla</td>
<td>Con 1 se hace una captura de pantalla; después se reinicia automáticamente</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60603</td>
<td>Ubicación de las capturas</td>
<td>0-memoria USB</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60604</td>
<td>Activar la protección del HMI</td>
<td>Con 1 se usa la protección del HMI</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60605</td>
<td>Número de niveles de contraseña de la protección del HMI</td>
<td>Número de niveles de contraseña de la protección del HMI, máximo 15</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60606-60835</td>
<td>Periodo de validez de la protección del HMI</td>
<td>60606-60628: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 1, y contraseña de desbloqueo (16 caracteres)<br />
60629-60651: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 2, y contraseña de desbloqueo (16 caracteres)<br />
60652-60674: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 3, y contraseña de desbloqueo (16 caracteres)<br />
60675-60697: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 4, y contraseña de desbloqueo (16 caracteres)<br />
60698-60720: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 5, y contraseña de desbloqueo (16 caracteres)<br />
60721-60743: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 6, y contraseña de desbloqueo (16 caracteres)<br />
60744-60766: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 7, y contraseña de desbloqueo (16 caracteres)<br />
60767-60789: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 8, y contraseña de desbloqueo (16 caracteres)<br />
60790-60812: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 9, y contraseña de desbloqueo (16 caracteres)<br />
60813-60835: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 10, y contraseña de desbloqueo (16 caracteres)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63000-63114</td>
<td>Periodo de validez de la protección del HMI</td>
<td>63000-63022: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 11, y contraseña de desbloqueo (16 caracteres)<br />
63023-63045: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 12, y contraseña de desbloqueo (16 caracteres)<br />
63046-63068: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 13, y contraseña de desbloqueo (16 caracteres)<br />
63069-63091: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 14, y contraseña de desbloqueo (16 caracteres)<br />
63092-63114: año, mes, día, hora, minuto, segundo y pantalla de aviso al caducar la contraseña de nivel 15, y contraseña de desbloqueo (16 caracteres)</td>
<td></td>
</tr>
<tr class="odd">
<td>63115~63130</td>
<td>Dirección de entrada para cambiar la contraseña de nivel superior</td>
<td>63115~63131: dirección para cambiar la contraseña de nivel superior (16 caracteres); tras introducirla, escriba 1 en LW63131 para aplicarla</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63131</td>
<td>Dirección de activación de la contraseña de nivel superior</td>
<td>63115~63130: tras introducir la contraseña de nivel superior, escriba 1 en esta dirección para aplicarla</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60836</td>
<td>Guardar en el HMI</td>
<td>Con 1 se guardan en el HMI los ajustes de la protección del HMI; después se reinicia automáticamente.</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60837</td>
<td>Reiniciar la protección del HMI</td>
<td>Devuelve la protección del HMI a su estado inicial. Los usuarios ya desbloqueados deben desbloquear de nuevo</td>
<td>W</td>
</tr>
<tr class="odd">
<td>60997</td>
<td>Uso de la entrada USB.</td>
<td>Por defecto 0: teclado o ratón USB. Con 1: lector de códigos de barras</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60998</td>
<td>Carácter final del lector de códigos 2D USB: 0-ENTER, 1-TAB+ENTER</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>60999</td>
<td>Longitud de código del lector 2D USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61000 - 61127</td>
<td>Almacenamiento y uso del código 2D leído</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61128</td>
<td>Uso de los parámetros de impresora</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61138</td>
<td>Importación de receta: ID de la receta origen</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61139</td>
<td>Importación de receta: ID de la receta destino</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61140</td>
<td>ID de la receta a borrar</td>
<td>-1 si el valor inicial se muestra como entero de 16 bits; si no, 65535</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61141</td>
<td>Cambia el grupo de recetas actual con el HMI en marcha</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="even">
<td>61143</td>
<td>Número de grupo para importar/exportar recetas por memoria USB</td>
<td></td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>61146</td>
<td>Número de la ventana a imprimir en la impresión controlada por registro</td>
<td>Introduzca el número de la ventana a imprimir y active LB60175 para lanzar la impresión (reinicio automático)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62020-62039</td>
<td>Nombre de la receta actual</td>
<td>Visualización ASCII, codificación Unicode, longitud 20; muestra el nombre de la receta actual</td>
<td>R</td>
</tr>
<tr class="odd">
<td>62040</td>
<td>Selección del nivel de inicio de sesión</td>
<td>Nivel de usuario con el que se inicia sesión; corresponde al nivel activado en «Parámetros de la pantalla táctil» → «Contraseñas de usuario»</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>62041~62056</td>
<td>Dirección de entrada de la contraseña de inicio de sesión</td>
<td>Introduzca la contraseña del nivel definido en 62040. La contraseña de nivel superior desbloquea todos los niveles (16 caracteres) y completa el inicio de sesión.</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>62057</td>
<td>Registro del número de prórrogas del HMI</td>
<td>Si la opción de prórroga está activada en la protección del HMI, aquí se modifica el número de prórrogas; valor por defecto 1</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63141~63146</td>
<td>Fecha de caducidad de la contraseña dinámica</td>
<td>Año, mes, día, hora, minuto, segundo: LW63141~63146, entero de 16 bits; tras introducir la fecha, active LB60182 para aplicarla (reinicio automático)</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63147~63152</td>
<td>Dirección de la clave de la contraseña dinámica</td>
<td>Modifica la clave de la contraseña dinámica, dirección LW63147, tipo ASCII, longitud 6; active LB60179 para aplicarla (reinicio automático)</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63153~63184</td>
<td>Cambiar el nombre de la receta</td>
<td>Entrada ASCII, longitud 32; el cambio se aplica con LB60180</td>
<td>W</td>
</tr>
<tr class="odd">
<td>63186~63189</td>
<td>Dirección IP del equipo Ethernet</td>
<td>Dirección IP del equipo Ethernet en modo estándar, entero de 16 bits. Tras ajustar IP, puerto y número de estación, active LB60178 para aplicarlos</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>63190</td>
<td>Número de estación del equipo Ethernet</td>
<td>Número de estación del equipo Ethernet en modo estándar, entero de 16 bits. IP, puerto y número de estación se aplican con LB60178</td>
<td>R/W</td>
</tr>
<tr class="odd">
<td>63191</td>
<td>Puerto del equipo Ethernet</td>
<td>Puerto del equipo Ethernet en modo estándar, entero de 16 bits. Tras ajustar IP, puerto y número de estación, active LB60178 para aplicarlos</td>
<td>R/W</td>
</tr>
<tr class="even">
<td>60838~60853</td>
<td>Nombre del usuario conectado</td>
<td>Gestión de permisos: muestra el nombre del usuario conectado; objeto: visualización ASCII, longitud 32</td>
<td>R</td>
</tr>
<tr class="odd">
<td>63200~63215</td>
<td>Grupo del usuario conectado</td>
<td>Gestión de permisos: muestra el grupo del usuario conectado (su primer grupo); objeto: visualización ASCII, longitud 32</td>
<td>R</td>
</tr>
</tbody>
</table>
