# 🚀 00 - Introdução ao Mundo Arduino

Bem-vindo ao ponto de partida do **IoT Tutorials**! Se você nunca usou um Arduino antes, este guia é para você. Vamos passar pelos conceitos básicos para que você se sinta confortável para montar os outros projetos do repositório.

## 1. O que é um Arduino?

![Arduino Uno](https://storage.googleapis.com/stateless-media-prod-328/media/2023/06/f0e3479a-arduino-uno-r3.png)

O Arduino é uma pequena placa de prototipagem eletrônica, como um "mini-computador". Ele permite que você crie objetos interativos, lendo informações do ambiente através de sensores e controlando luzes, motores e outros atuadores.

- **É o cérebro:** Nos nossos projetos, o Arduino será o cérebro que decide quando regar a planta ou quando acender uma luz.
- **É de código aberto:** Tanto o hardware (a placa) quanto o software (o programa) são livres, o que significa que existe uma comunidade gigante criando projetos e tirando dúvidas.

## 2. O que é a Arduino IDE?

A **IDE (Ambiente de Desenvolvimento Integrado)** do Arduino é o programa que você instala no seu computador para escrever o código e enviá-lo para a sua placa Arduino.

- **Onde baixar:** Você pode baixar a versão mais recente gratuitamente no site oficial: **[arduino.cc/en/software](https://www.arduino.cc/en/software)**

## 3. Seu Primeiro Código: O "Blink" (Pisca-Pisca)

O "Hello, World!" do mundo do hardware é fazer um LED piscar. Felizmente, a maioria das placas Arduino já vem com um LED embutido, conectado ao pino 13.

Abra sua Arduino IDE, cole o código abaixo e vamos ver a mágica acontecer!

```cpp
/*
  Blink - O "Olá, Mundo!" do Arduino
  Este código liga o LED embutido na placa por 1 segundo,
  depois desliga por 1 segundo, repetidamente.
*/

// A função setup() é executada uma única vez quando a placa é ligada.
// É usada para configurações iniciais.
void setup() {
  // Configura o pino 13 (onde o LED está) como um pino de SAÍDA (OUTPUT).
  pinMode(13, OUTPUT);
}

// A função loop() é executada continuamente, sem parar,
// logo após a função setup() terminar.
void loop() {
  digitalWrite(13, HIGH);   // Envia um sinal ALTO (HIGH) para o pino 13 (liga o LED)
  delay(1000);              // Espera por 1000 milissegundos (1 segundo)
  digitalWrite(13, LOW);    // Envia um sinal BAIXO (LOW) para o pino 13 (desliga o LED)
  delay(1000);              // Espera por 1 segundo
}
```

## 4. Como Carregar o Código para a Placa

1.  **Conecte o Arduino:** Use um cabo USB para conectar sua placa ao computador.
2.  **Selecione a Placa:** Na IDE, vá em `Ferramentas > Placa` e selecione o modelo da sua placa (ex: "Arduino Uno").
3.  **Selecione a Porta:** Vá em `Ferramentas > Porta` e selecione a porta em que o Arduino apareceu (ex: `COM3` no Windows ou `/dev/ttyUSB0` no Linux).
4.  **Clique em Carregar:** Clique no botão com uma seta para a direita (→) na parte superior da IDE.

Após alguns segundos, a IDE mostrará a mensagem "Carregado". Você verá o pequeno LED na sua placa piscando!

## Próximos Passos

Parabéns! Você acabou de programar um Arduino. Agora que você entende o básico de `setup()`, `loop()`, `digitalWrite()` e `delay()`, está pronto para explorar os outros tutoriais e começar a interagir com o mundo real!
