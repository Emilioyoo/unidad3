# Unidad 3
Jonatha Emilio Yañez Olvera
<br>
GDS0641

## Link TikTok
https://vm.tiktok.com/ZMkRAwKe2/

## software a utilizar
|Software|Versión|
|--|--|
|Thonny|4.1.6|
|TikTok||

## Materiales a utilizar
| Material | Imagen | Cantidad | Costo |
|----------|--------|----------|-------|
| ESP32    | <img src="https://github.com/user-attachments/assets/0d280367-493e-4f7c-a587-36e1f822116b" width="100"/> | 1 | 120.00 |
| Servo motor  | <img src="https://m.media-amazon.com/images/I/51ZhuPCUauL._AC_UF894,1000_QL80_.jpg" width="100"/> | 2 | 89.00 |
|   Buzzer   |     <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcT2Uex9EaVH0t9VSWeqHC4T4kqgwmRSdmPtPs6Bym2Eh6qONbHuEYl-q0GPq9c_qOwTvFpXFIkd_iKgEQ0s-ocg3K6gz20E-gT0spYL_tjXi6lDQFQtG-QXhw&usqp=CAE" width="100"/>     |     1  |  69     |
|Cable tipo C |<img src="https://github.com/user-attachments/assets/f9dd0a9b-400d-422a-89b6-8141bbe10e68" width="100"/> | 1 |35|
|Cableado para conexiones |<img src="https://m.media-amazon.com/images/I/71fdyWUFT8L.jpg" width="100"/> | Varios |80|
|Cutter |<img src="https://www.construactivo.com/5896-large_default/cutter-profesional-alma-metalica-18mm-truper.jpg" width="100"/> | 1  |15|
|Silicona Caliente |<img src="https://i.pinimg.com/736x/e9/57/cc/e957ccedc373cd614b2b0b99678acb0d.jpg" width="100"/> | 1  |50|
| Globo |<img src="https://github.com/user-attachments/assets/c21947ac-1ff9-4ad9-aef8-eeffff8a4ff2" width="100"/> | 1  |15|
| Papel periodico |<img src="https://github.com/user-attachments/assets/44dd9811-6f14-4c4f-86d2-495384c75892" width="100"/> | Varios  |16|
| Resistol liquido |<img src="https://github.com/user-attachments/assets/e99c357b-66ae-49ed-bc82-c1ec349545ff" width="100"/> | 1  |15|
| Foami  |<img src="https://github.com/user-attachments/assets/df52a2d3-2861-4342-ae9f-1b4dee3d0d5e" width="100"/> | 1  |105|
| Carton  |<img src="https://github.com/user-attachments/assets/30d054e9-db29-4806-ab1f-aba71f4d3c85" width="100"/> | 1  |105|
| Pintura |<img src="https://github.com/user-attachments/assets/dfd5b22c-1f65-47c6-9956-393a27cf44af" width="100"/> | 1  |65|
| Esfera Transparente |<img src="https://github.com/user-attachments/assets/1e6b91e2-c1d6-4747-8fc4-07ce6c67d49e" width="100"/> | 2  |25|
|Tira LED |<img src="https://github.com/user-attachments/assets/6f3409d6-e7f4-4f0b-8707-2140636846c3" width="100"/> | 1 |155|

## Fotos del proceso
<br>
<img src="https://github.com/user-attachments/assets/730669e0-8ddc-4369-83ab-9e6dec35dc03" width="250"/>
<img src="https://github.com/user-attachments/assets/d8563f74-47b4-4b0c-8908-c679e6b8c751" width="250"/>

## Codigo de Node-Red
[
    {
        "id": "1038ee9b08765c63",
        "type": "tab",
        "label": "Flow 3",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "cc2315206565d2fa",
        "type": "ui_button",
        "z": "1038ee9b08765c63",
        "name": "",
        "group": "c7520ffc2839024f",
        "order": 2,
        "width": 0,
        "height": 0,
        "passthru": false,
        "label": "buttonov",
        "tooltip": "",
        "color": "",
        "bgcolor": "",
        "className": "",
        "icon": "",
        "payload": "PRESS",
        "payloadType": "str",
        "topic": "nodered/button",
        "topicType": "str",
        "x": 360,
        "y": 200,
        "wires": [
            [
                "91a614630691e99f"
            ]
        ]
    },
    {
        "id": "a4303be754270200",
        "type": "ui_switch",
        "z": "1038ee9b08765c63",
        "name": "",
        "label": "switchOV",
        "tooltip": "",
        "group": "c7520ffc2839024f",
        "order": 3,
        "width": 0,
        "height": 0,
        "passthru": true,
        "decouple": "false",
        "topic": "nodered/switch",
        "topicType": "str",
        "style": "",
        "onvalue": "ON",
        "onvalueType": "str",
        "onicon": "",
        "oncolor": "",
        "offvalue": "OFF",
        "offvalueType": "str",
        "officon": "",
        "offcolor": "",
        "animate": false,
        "className": "",
        "x": 320,
        "y": 320,
        "wires": [
            [
                "135f82da33bb2f74"
            ]
        ]
    },
    {
        "id": "91a614630691e99f",
        "type": "mqtt out",
        "z": "1038ee9b08765c63",
        "name": "musicov",
        "topic": "nodered/button",
        "qos": "2",
        "retain": "true",
        "respTopic": "",
        "contentType": "",
        "userProps": "",
        "correl": "",
        "expiry": "",
        "broker": "e0dd5710309997b4",
        "x": 620,
        "y": 180,
        "wires": []
    },
    {
        "id": "135f82da33bb2f74",
        "type": "mqtt out",
        "z": "1038ee9b08765c63",
        "name": "ledsov",
        "topic": "nodered/switch",
        "qos": "2",
        "retain": "true",
        "respTopic": "",
        "contentType": "",
        "userProps": "",
        "correl": "",
        "expiry": "",
        "broker": "e0dd5710309997b4",
        "x": 610,
        "y": 280,
        "wires": []
    },
    {
        "id": "c7520ffc2839024f",
        "type": "ui_group",
        "name": "Si",
        "tab": "203f978d7e8d6d83",
        "order": 5,
        "disp": true,
        "width": "6",
        "collapse": false,
        "className": ""
    },
    {
        "id": "e0dd5710309997b4",
        "type": "mqtt-broker",
        "name": "",
        "broker": "broker.emqx.io",
        "port": "1883",
        "clientid": "",
        "autoConnect": true,
        "usetls": false,
        "protocolVersion": "4",
        "keepalive": "60",
        "cleansession": true,
        "autoUnsubscribe": true,
        "birthTopic": "",
        "birthQos": "0",
        "birthRetain": "false",
        "birthPayload": "",
        "birthMsg": {},
        "closeTopic": "",
        "closeQos": "0",
        "closeRetain": "false",
        "closePayload": "",
        "closeMsg": {},
        "willTopic": "",
        "willQos": "0",
        "willRetain": "false",
        "willPayload": "",
        "willMsg": {},
        "userProps": "",
        "sessionExpiry": ""
    },
    {
        "id": "203f978d7e8d6d83",
        "type": "ui_tab",
        "name": "Dashboard",
        "icon": "dashboard",
        "order": 1,
        "disabled": false,
        "hidden": false
    }
]
## Codigo Python
import time
import network
from umqtt.simple import MQTTClient
from machine import Pin

# Configuración del broker MQTT
MQTT_BROKER = "broker.emqx.io"
MQTT_USER = ""
MQTT_PASSWORD = ""
MQTT_CLIENT_ID = "esp32_motor_client"
MQTT_TOPIC_PROXIMIDAD = "bldh/proximidad"
MQTT_PORT = 1883

# Definir los pines de control del motor
IN1 = Pin(27, Pin.OUT)
IN2 = Pin(14, Pin.OUT)
IN3 = Pin(12, Pin.OUT)
IN4 = Pin(13, Pin.OUT)

# Secuencia para el motor a pasos (estilo paso completo)
sec_anticlockwise = [
    [1, 0, 0, 1],
    [1, 0, 0, 0],
    [1, 1, 0, 0],
    [0, 1, 0, 0],
    [0, 1, 1, 0],
    [0, 0, 1, 0],
    [0, 0, 1, 1],
    [0, 0, 0, 1]
]

sec_clockwise = [
    [0, 0, 0, 1],
    [0, 0, 1, 1],
    [0, 1, 1, 0],
    [0, 1, 0, 0],
    [1, 1, 0, 0],
    [1, 0, 0, 0],
    [1, 0, 0, 1],
    [1, 0, 1, 0]
]

# Función para conectar a WiFi
def conectar_wifi():
    sta_if = network.WLAN(network.STA_IF)
    sta_if.active(True)
    sta_if.connect('UTNG_GUEST', 'R3d1nv1t4d0s#UT')  # Cambia esto por tu red WiFi
    while not sta_if.isconnected():
        time.sleep(0.3)
    print("WiFi Conectada!")

# Función para conectar al broker MQTT
def conectar_mqtt():
    client = MQTTClient(MQTT_CLIENT_ID, MQTT_BROKER, port=MQTT_PORT, user=MQTT_USER, password=MQTT_PASSWORD)
    try:
        client.connect()
        print("Conectado al broker MQTT")
    except Exception as e:
        print(f"Error al conectar con MQTT: {e}")
        client = None
    return client

# Función para mover el motor en sentido horario
def mover_motor_clockwise(pasos, retardo=0.001):
    for _ in range(pasos):
        for secuencia in sec_clockwise:
            IN1.value(secuencia[0])
            IN2.value(secuencia[1])
            IN3.value(secuencia[2])
            IN4.value(secuencia[3])
            time.sleep(retardo)

# Función para mover el motor en sentido antihorario
def mover_motor_anticlockwise(pasos, retardo=0.001):
    for _ in range(pasos):
        for secuencia in sec_anticlockwise:
            IN1.value(secuencia[0])
            IN2.value(secuencia[1])
            IN3.value(secuencia[2])
            IN4.value(secuencia[3])
            time.sleep(retardo)

# Función para manejar los mensajes MQTT
def llegada_mensaje(topic, msg):
    print("Mensaje recibido:", msg)
    if topic == b"bldh/proximidad" and msg == b"proximo":
        # Activar el motor cuando se recibe el mensaje
        mover_motor_clockwise(200)  # Gira el motor en sentido horario
        time.sleep(1)
        mover_motor_anticlockwise(200)  # Gira el motor en sentido antihorario

# Función para suscribirse al broker MQTT
def subscribir():
    client = conectar_mqtt()
    client.set_callback(llegada_mensaje)
    client.subscribe(MQTT_TOPIC_PROXIMIDAD)
    print("Esperando mensajes en el tópico:", MQTT_TOPIC_PROXIMIDAD)
    return client

# Main loop
#def main():
#    conectar_wifi()
#    client = subscribir()

#    while True:
#        client.check_msg()  # Verificar si hay nuevos mensajes MQTT

#if name == 'main':
#main()
conectar_wifi()
client = subscribir()

while True:
    client.wait_msg()

## Curso JavaScript en Netacad 

-- EXAMENES--
<br>
<img src="https://github.com/user-attachments/assets/a96ec9e9-9ea7-4544-a1d8-61c4041e0c10" width="500"/>
<br>
