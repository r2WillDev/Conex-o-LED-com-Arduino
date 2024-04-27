# Conexão-LED-com-Arduino

>[!NOTE]
>Todo o projeto está disponível no meu perfil no [Tinkercard](https://www.tinkercad.com/things/61z2brH3l1v-conexao-led-com-o-arduino?sharecode=Sg2ym6PjBLobUdnRyUxfOiIvHEMOElWz4xsYSS5Or_k)

Projeto desenvolvido como atividade na faculdade

## Hardware

- LED 1x
- Placa de ensaio pequena
- Arduino Uno R3

![image](https://github.com/r2WillDev/Conex-o-LED-com-Arduino/assets/106842143/db3a9c5e-138c-488a-b6b0-836944fc7d8b)

## Código

1. Define o pino número 10 como ledPin, que será usado para controlar um LED.
2. Na função **setup()**:
   - Configura o ledPin como uma saída usando a função **pinMode()**. Isso é necessário para enviar sinais digitais ao LED.
3. Na função **loop()** que é executada repetidamente:
   - Liga o LED enviando um sinal **HIGH (alto)** para o ledPin com a função **digitalWrite()**.
   - Mantém o LED ligado por **3000 milissegundos (3 segundos)** usando a função **delay()**.
   - Desliga o LED enviando um sinal **LOW (baixo)** para o ledPin.
   - Mantém o LED desligado por **5000 milissegundos (5 segundos)** antes de repetir o ciclo.

Resumindo, este código faz um LED piscar: ele fica ligado por 3 segundos e desligado por 5 segundos, repetindo esse padrão indefinidamente enquanto o Arduino estiver ligado e rodando o programa.

```

// C++ code
//
int ledPin = 10;
void setup()
{
  pinMode(ledPin, OUTPUT);
}

void loop()
{
  digitalWrite(ledPin, HIGH);
  delay(3000); // Wait for 3000 millisecond(s)
  digitalWrite(ledPin, LOW);
  delay(5000); // Wait for 5000 millisecond(s)
}

```
