<h1 align="center">Projeto Diaphora</h1>
<div align="center" >
<img src="https://github.com/claranevess/diaphora/assets/166565110/16511514-8892-4b20-9ebf-0ea0a4088369 alt="Imagem Arredondada" style="width: 40%;  border-radius: 50%;">
</div>

# 💻Projeto Diaphorá
<p align="center">O projeto Diaphora é uma solução inovadora destinada a auxiliar psicopedagogo e psicólogos no apoio a pessoas com Transtorno de Déficit de Atenção e Hiperatividade (TDAH) a melhorar a sua concentração e habilidades de foco no dia a dia. O dispositivo principal do projeto é uma caixa equipada com um sistema de reforço positivo que só é aberta após a execução de uma determinada sequência de luzes.</p>

# ⚙️Componentes
## Arduino Uno
● Botões
● LEDs
● Resistores
● Jumpers
● Servo Motor
● lCD
## Ligações dos Componentes no Arduino
1º. Servo Motor

- Pino de Sinal: Conecte ao pino digital 11 do Arduino.
- Pino de Energia (VCC): Conecte ao pino 5V do Arduino.
- Pino de Terra (GND): Conecte ao pino GND do Arduino.
  
2º. Botões
- Botão Verde:
- Um pino do botão: Conecte ao pino digital 2 do Arduino.
- Outro pino do botão: Conecte ao GND do Arduino (com pull-up interno ativado
no código).
- Botão Vermelho:
- Um pino do botão: Conecte ao pino digital 3 do Arduino.
- Outro pino do botão: Conecte ao GND do Arduino (com pull-up interno ativado
no código).

3º. LEDs RGB
- Os LEDs RGB têm três pinos: um pino comum (anodo ou catodo) e dois pinos para
controlar as cores. Neste caso, estamos usando LEDs RGB ou LEDs comuns de cores
diferentes, então cada LED terá seu próprio pino de controle.
- LED Verde 1: Conecte ao pino digital 4 do Arduino.
- LED Vermelho 1: Conecte ao pino digital 5 do Arduino.
- LED Verde 2: Conecte ao pino digital 6 do Arduino.
- LED Vermelho 2: Conecte ao pino digital 7 do Arduino.
- LED Verde 3: Conecte ao pino digital 8 do Arduino.
- LED Vermelho 3: Conecte ao pino digital 9 do Arduino.
Para cada LED:
- Pino de Controle do LED: Conecte ao pino correspondente do Arduino (conforme listado
acima).
- Pino Comum do LED (anodo ou catodo):
- Se estiver usando LEDs comuns (comum cátodo), conecte o pino comum ao
GND do Arduino.
- Se estiver usando LEDs RGB (comum ânodo), conecte o pino comum ao 5V do
Arduino.
 
4º. Resistores 
- Para proteger os LEDs e garantir que eles funcionem corretamente, utilize
resistores.
- Resistores de 220 ohms (ou valor adequado para os LEDs em uso) devem ser
conectados em série com cada LED.
# Diagrama de Ligações
- |Arduino|-------------------------------------------|Componentes|
- GND------------------------------------------------> GND do Servo Motor
- 5V--------------------------------------------------> VCC do Servo Motor
- pino 11---------------------------------------------> Pino de Sinal do Servo Motor
- pino 2----------------------------------------------> Um pino do Botão Verde
- GND------------------------------------------------> Outro pino do Botão Verde (Pull-up interno)
- pino 3----------------------------------------------> Um pino do Botão Vermelho
- GND------------------------------------------------> Outro pino do Botão Vermelho (Pull-up interno)
- pino 4----------------------------------------------> LED Verde 1 (via resistor)
- pino 5----------------------------------------------> LED Vermelho 1 (via resistor)
- pino 6----------------------------------------------> LED Verde 2 (via resistor)
- pino 7----------------------------------------------> LED Vermelho 2 (via resistor)
- pino 8----------------------------------------------> LED Verde 3 (via resistor)
- pino 9----------------------------------------------> LED Vermelho 3 (via resistor)
- GND/5V--------------------------------------------> Pino comum dos LEDs (dependendo do tipo de LED)

# 📝Funcionamento do Codigo
- setup()  
Inicializa as configurações do Arduino, incluindo pinos, LCD e servos.
- loop()  
Loop principal que chama as funções de controle de cronômetro, botões e atualização do LCD.
- controleCronometro()  
Verifica o estado dos botões de início e pausa para controlar o cronômetro.
- controleBotoes()  
Lê o estado dos botões verde e vermelho e chama as funções apropriadas para cada um.
- trataBotaoVerde()  
Atualiza o estado dos LEDs RGB e contadores quando o botão verde é pressionado.
- trataBotaoVermelho()  
Atualiza o estado dos LEDs RGB e contadores quando o botão vermelho é pressionado.
- verificaCondicoesLEDs()  
Verifica se três LEDs verdes ou vermelhos estão acesos e controla os servos de acordo.
- resetaLEDs()  
Desliga todos os LEDs RGB.
- atualizaCronometro()  
Atualiza o cronômetro no LCD quando ele está em execução.
##  Bibliotecas Utilizadas
- Wire.h: Comunicação I2C para o LCD.
- LiquidCrystal_I2C.h: Controle do LCD via I2C.
- Servo.h: Controle dos servos motores.
## 🙋‍♂️ Criado por:
- [Matheus Lustosa](https://github.com/MatheusLustosa).
- 
