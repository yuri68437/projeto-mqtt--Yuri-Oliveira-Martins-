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

[![gmailLogo](https://user-images.githubusercontent.com/61972825/106656703-cb3aab00-6579-11eb-9193-83d099d4e68a.jpg)
](https://user-images.githubusercontent.com/61972825/106656084-f7096100-6578-11eb-8fcc-06c1c17311ad.jpg)](https://www.google.com/search?q=gmail&oq=gmail&aqs=chrome.0.69i59l3j69i60l3j69i61l2.747j0j4&sourceid=chrome&ie=UTF-8)
