# Entregável Projeto Arduíno e MQTT
---
## OBJETIVO
---  

O objetivo desse projeto é utilizar um Arduino **UNO** e um Sensor Magnético para monitorar se a porta de um rack de rede está **ABERTO** ou **FECHADO**.

Enviar essa informação via internet utilizando o protocolo MQTT(*Message Queuing Telemetry Transport*) para um servidor MQTT hospedado na Amazon web Service(*AWS*) e exibir a informação em um cliente MQTT[*MQTT Dash](https://play.google.com/store/apps/details?id=net.routix.mqttdash&hl=pt_BR&gl=US), instalado em um Smartphone, conforme imagem abaixo;

![img1](https://user-images.githubusercontent.com/61972825/106648875-9fb2c300-656f-11eb-8c33-3fe701f12e50.jpg)

Foram utilizando as seguintes bibliotecas: 

* [UIPEthernet](https://github.com/UIPEthernet/UIPEthernet) (conexão do ENC28J60 com o Arduíno)
* [PubSubClient](https://github.com/knolleary/pubsubclient)(cliente MQTT para o arduino)
