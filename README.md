<p align="center"><img src="https://i.imgur.com/A6bWGFl.gif"/></p>

<h1 align="center">Quinto Flow </h1>

<h4> Este repositorio contiene el Quinto ejercicio en Node Red,El flow 5 representa el Quinto ejercicio a realizar con NodeRed. Este flow consiste en un tablero que un conjunto de gráficas en Dasboard, las cuales tienen como proposito reportar la información climática recibida manualmente por MQTT, la información recibida automáticamente por API y la información de varius usuarios compartida por MQTT en un broker publico </h4> 


### CONTENIDO
#### Material necesario
- Node.js Usar la versión LTS v16x e instalar los build tools.
- Node-Red
- Nodos Dashboard
-Mosquitto
#### Instrucciones
1.Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
2.Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2
3.Instalar los nodos node-red-dashboard. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.
4.Instalación de Broker local Mosquitto MQTT.
#### Instrucciones de operacion
- Arrancar NodeRed con el comando <code> node-red </code>
- Importar el flow del repositorio.
- Coloca tu API Key personal en la API Call del nodo HTTP Request.
- Actualiza la IP del broker público.
- Hacer clic en el boton Deploy.
- Para observar el resutlado de este flow, abre un navegador y dirígete a localhost:1880/ui
- Para activar las gráficas de clima manual, debes enviar por MQTT un mensaje que contenga un JSON con las variables ID, temp y hum.

#### Notas
- La sección manual de este flow se suscribe al tema codigoIoT/fow5/mqtt en un broker local.
- El mensaje mqtt usado para probar este flow es mosquitto_pub -h localhost -t ccodigoIoT/fow5/mqtt -m '{"ID":"Alejandro Flores","temp":18,"hum":78}'
- Para que la gráfica historica muestre información, deben enviarse al menos 2 puntos.
- Para actualizar la IP del broker publico, se recomienda el siguiente comando nslookup broker.hivemq.com. Puedes usar el broker publico de tu elección.
- Para que multiples graficas sean mostradas en la sección de Histórico Público, es necesario que multiples usuarios se encuentren publicando a la vez.
- Para enviar mensaje al broker escribir la siguiente linea en terminal <code> mosquitto_pub -h 3.124.50.83  -t codigoIoT/flow5/mqtt/clima -m '{"ID":"Alejandro Flores Mor Acatlipa","temp":18,"hum":78}'</code>
- Para suscribirse y ver las publicaciones a traves de la terminal escribir este code en la terminal <code> mosquitto_sub -h 3.124.50.83 -t codigoIoT/flow5/mqtt/clima </code>
#### Resultados y conclusiones 

A continuación puede ver el tablero resultante.<a href="https://www.mozilla.org/es-ES/">tablero</a>.
A continuación puedes ver los nodos del flow.<a href="https://www.mozilla.org/es-ES/">tablero</a>.
#### Video representativo
Puedes encontrar el video del funcionamiento en el siguiente enlace: <a href="https://www.mozilla.org/es-ES/">Video</a>.
