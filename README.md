#Sensor-de-Luminosidade

Este repositório trata-se de um artigo feito por mim enquanto formanda da Universidade Presbiteriana Mackenzie, onde crio um protótipo de IOT capaz de analisar a luminosidade do ambiente

O protótipo consiste em medir e capitar a variação de luminosidade do ambiente. Para isso foi utilizado o sensor LDR para fazer a leitura da luminosidade do ambiente. Podemos utilizá-lo em ambientes onde existem necessidade de medição de luminosidade com o fim de regular a iluminação do ambiente.

Utilizaremos a IDE arduinoi.cc para desenvolver nossa programação do protótipo de luminosidade, ela foi criada para fazer a leitura dos dados do LDR.

Os componentes utilizados para a construção do protótipo foram:

Neste projeto foram utilizados os seguintes componentes:

>1 placa Arduino Uno R3 

>1 Cabo USB A macho B fêmea


>1 LDR de 5mm

>1 Resistor de 10 k

>1 resistor de 220 ohm

>5 cabos macho macho

>1 protoboard de 400

>1 led



Abaixo um passo a passo dos comandos que foram utilizados:




int LED = 8;      // vamos instanciar uma variável para o atuador escolhido, que nesse caso foi o led, onde se encontra conectado ao pin 8


void setup() 



{

Serial.begin(9600);   // vamos fazer o setup do serial da placa Arduino, o valor é padrão



pinMode(LED, OUTPUT);   // representa a saída do led, onde poderemos liga-lo e desliga-lo.


}


void loop()

{

int LDR = analogRead(A0);   // vamos ler o valor na porta análoga A0 e armazenando na variável chamada LDR



 Serial.println(LDR);   // Vamos mostrar na tela o valor armazenado na variável LDR

 
    if(LDR<500)
    
    digitalWrite(LED,HIGH);   // se o valor do LDR for “menor” do que 500 o led será ligado
    
  else
  
     digitalWrite(LED,LOW);   // se não, o led será desligado
     
   delay(500);     // o delay representa a velocidade que os valores serão exibidos no monitor serial. Importante deixá-lo baixo para que não haja a depreciação dos componentes.
   
} 

