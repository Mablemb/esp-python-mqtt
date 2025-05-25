# ESP Python MQTT

Projeto de integração entre um dispositivo embarcado ESP32 e um backend Python utilizando o protocolo MQTT, com o broker Mosquitto.

## Descrição

Este projeto demonstra como conectar um ESP32 a um broker MQTT (Mosquitto), publicar mensagens de teste e receber essas mensagens em um backend Python. O objetivo é servir de base para aplicações IoT, automação residencial, monitoramento de sensores, entre outros.

## Estrutura do Projeto

```
esp-python-mqtt/
│
├── backend/
│   └── client.py              # Cliente Python que se conecta ao broker MQTT
│
├── embarcado/
│   └── espcomunication.ino    # Código Arduino para ESP32 publicar mensagens MQTT
│
├── configuracoes/
│   └── mosquitto.conf         # Exemplo de configuração do broker Mosquitto
│
└── readme.txt                 # Instruções e anotações iniciais
```

## Pré-requisitos

- ESP32 com Arduino IDE configurado
- Python 3.x
- Broker MQTT (Mosquitto)
- Biblioteca PubSubClient para Arduino
- Biblioteca paho-mqtt para Python

## Instalação

### 1. Configurar o Broker MQTT

- Instale o Mosquitto em sua máquina ou utilize um broker na nuvem.
- Utilize o arquivo `configuracoes/mosquitto.conf` como base para configuração.
- Inicie o serviço Mosquitto.

### 2. Configurar o ESP32

- Abra o arquivo `embarcado/espcomunication.ino` na Arduino IDE.
- Altere as variáveis `ssid`, `password` e `mqtt_server` para os valores da sua rede e broker.
- Instale a biblioteca PubSubClient via Gerenciador de Bibliotecas.
- Faça o upload do código para o ESP32.

### 3. Configurar o Backend Python

- Instale a biblioteca paho-mqtt:
  ```powershell
  pip install paho-mqtt
  ```
- Edite o arquivo `backend/client.py` e ajuste o IP do broker MQTT se necessário.
- Execute o backend:
  ```powershell
  python backend\client.py
  ```

## Funcionamento

- O ESP32 conecta-se ao Wi-Fi e ao broker MQTT, publicando mensagens periódicas no tópico `topico/teste`.
- O backend Python se conecta ao mesmo broker e escuta o tópico, exibindo as mensagens recebidas.

## Testes

- Verifique no monitor serial do Arduino IDE se o ESP32 está publicando as mensagens.
- No terminal, o backend Python deve exibir as mensagens recebidas.

## Autor

- Nome: Henrique Mesquita
- Contato: github.com/Mablemb
