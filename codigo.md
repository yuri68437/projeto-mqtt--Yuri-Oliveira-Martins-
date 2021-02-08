
~~~c++
#include <PubSubClient.h>
#include <UIPEthernet.h>
#include <utility/logging.h>
#include <SPI.h>

//Define o endereço MAC que será utilizado
byte mac[] = {0x90, 0x70, 0x0B, 0x87, 0xBB, 0xAA};
boolean msg;
int pino2 = 2;
boolean estado_sensor; 
//Inicia o cliente Ethernet
EthernetClient client;
PubSubClient mqttClient(client);

void setup() {
    //Inicia o controlador Ethernet e solicita um IP para o servidor de DHCP
    Ethernet.begin(mac);

    //Inicia o monitor Serial
    pinMode (pino2, INPUT_PULLUP);
    Serial.begin(9600);
    
    mqttClient.setServer("54.161.191.80",1883);

    //Exibe no Monitor Serial as informações sobre o IP do Arduino
    Serial.print("O IP do Arduino e: ");
    Serial.println(Ethernet.localIP());

    //Exibe no Monitor Serial as informações sobre a Máscara de Rede do Arduino
    Serial.print("A Mascara de Rede do Arduino e: ");
    Serial.println(Ethernet.subnetMask());

    //Exibe no Monitor Serial as informações sobre o Gateway do Arduino
    Serial.print("O Gateway do Arduino e: ");
    Serial.println(Ethernet.gatewayIP());

    //Exibe uma linha em branco
    Serial.println("");

}

void loop() {
    estado_sensor = digitalRead(pino2); //fazer a comparação 
    mqttClient.connect("aula91");
    if(estado_sensor == 1){ // fazer comparação para identificar se está ligado ou desligado
      Serial.println("O sensor esta aberto! ");      
      Serial.println(estado_sensor);
        msg = mqttClient.publish("aula91","Sensor ABERTO!");
    }else{ 
      Serial.println("O sensor esta fechado! ");      
      Serial.println(estado_sensor);
      msg = mqttClient.publish("aula91","Sensor FECHADO!");
    } 
  

  mqttClient.loop();
}
~~~

