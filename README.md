# Entregável Projeto Arduíno e MQTT
---
## OBJETIVO


O objetivo desse projeto é utilizar um Arduino **UNO** e um Sensor Magnético para monitorar se a porta de um rack de rede está **ABERTO** ou **FECHADO**.

Enviar essa informação via internet utilizando o protocolo MQTT(*Message Queuing Telemetry Transport*) para um servidor MQTT hospedado na Amazon web Service(*AWS*) e exibir a informação em um cliente MQTT[*MQTT Dash](https://play.google.com/store/apps/details?id=net.routix.mqttdash&hl=pt_BR&gl=US), instalado em um Smartphone, conforme imagem abaixo;

![img1](https://user-images.githubusercontent.com/61972825/106648875-9fb2c300-656f-11eb-8c33-3fe701f12e50.jpg)

Foram utilizando as seguintes bibliotecas: 

* [UIPEthernet](https://github.com/UIPEthernet/UIPEthernet)(conexão do ENC28J60 com o Arduino)
* [PubSubClient](https://github.com/knolleary/pubsubclient)(cliente MQTT para o arduino)  

## Materiais 
---

1. Arduíno uno  

2. Módulo Ethernet (ENC28J60)  

3. Sensor Magnético (MC-38)  

4. Jumpers  

## Circuito

![img2](https://user-images.githubusercontent.com/61972825/106652453-3ed9b980-6574-11eb-8ae9-f11237977850.jpg)
---
### Ligação dos Jumpers 

| PINOS ENC28J60 | Pinos Arduino |
| -------------- |:------------- | 
| 	CS       | 	10    	 | 
|	SI       |     	11	 |   
| 	SO       | 	12       |    
|      SCK	 | 	13	 |
|      VCC	 |     3.3 V	 |
|      GND	 |	GND    	 |
---

## Autor: Yuri Martins

[![gmail](https://user-images.githubusercontent.com/61972825/106668757-6b4c0080-6589-11eb-8da3-bfeaba4000aa.png)](https://mail.google.com/mail/u/0/#inbox?compose=new)

[![linkedinlogo](https://user-images.githubusercontent.com/61972825/106658428-0a69fb80-657c-11eb-9076-a4dc4e32762c.png)](https://br.linkedin.com/)

