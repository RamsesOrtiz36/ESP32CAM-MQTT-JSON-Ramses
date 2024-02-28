# ESP32CAM-MQTT-JSON-Ramses
Envío de mensaje tipo JSON desde ESP32CAM al Broker local por MQTT con valores aleatorios e identificación

Para esta parte se requiere tener instalados y configurados Mosquitto y node.js

Empezaremos por probar que funcione la comunicación con puro Mosquitto
Luego habilitamos Node-red
En node-red colocamos un nodo de comunicación para MQTT "mqtt in"
y lo enlazamos a un nodo "debug" para ver la recepción del mensaje

Para configurar el nodo de MQTT, 
  damos doble clic en el nodo
  editamos el servidor (boton con simbolo de lapiz)
    agregamos la IPv4 del servidor
    en caso de usar la computadora como host colocamos "localhost" 
    Aceptamos
  Ya con el servidor (host) declarado 
      Indicamos que solo aun tema se va a suscibir
      Colocomos el nombre del tema al que se quiere suscribir
  Cambiamos la Calidad del servicio a cero (0) CdS = QoS=0
Aceptamos los cambios dando clic al boton rojo de "Hecho" o "Done"
