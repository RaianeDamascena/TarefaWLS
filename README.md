# TarefaWLS


Este projeto foi desenvolvido com os seguintes objetivos principais:

- Compreender o funcionamento e a aplicação de comunicação serial em microcontroladores.
- Aplicar conhecimentos práticos sobre os protocolos UART e I2C.
- Manipular e controlar LEDs comuns e LEDs endereçáveis WS2812.
- Fixar o estudo do uso de botões de acionamento, interrupções e debounce.
- Desenvolver um projeto funcional que combine hardware e software.

## Descrição do Projeto
Este sistema foi projetado para integrar múltiplos componentes conectados a uma placa Raspberry Pi Pico. Os componentes utilizados incluem:

- **Matriz 5x5 de LEDs WS2812:** conectada à GPIO 7, utilizada para exibir números por meio de padrões luminosos.
- **LED RGB:** com os seguintes pinos conectados:
  - GPIO 11 para o LED verde.
  - GPIO 12 para o LED azul.
- **Botões:**
  - Botão A conectado à GPIO 5.
  - Botão B conectado à GPIO 6.
- **Display SSD1306:** conectado via I2C (GPIO 14 para SDA e GPIO 15 para SCL).

### Principais Funcionalidades:
- **Controle de LEDs:**
  - O botão A controla o estado do LED verde.
  - O botão B controla o estado do LED azul.
- **Exibição no Display SSD1306:**
  - O display mostra caracteres digitados no terminal serial.
  - Informações sobre o estado dos botões e LEDs são exibidas.
- **Matriz de LEDs:**
  - Quando números de 0 a 9 são digitados no terminal, esses são exibidos na matriz de LEDs.
  - Caso nenhum número seja exibido, a matriz é desligada.

### Controle por Interrupções
Os botões A e B utilizam interrupções para alternar o estado dos LEDs correspondentes. Um sistema de debounce com 200 ms foi implementado para evitar falsos acionamentos.

### Protocolo de Comunicação
A comunicação com o display é realizada por meio do protocolo I2C, com endereço padrão de 0x3C.

## Desenvolvido por
**Raiane Damascena**  
Email: [rai.paixao2012@gmail.com](mailto:rai.paixao2012@gmail.com)

