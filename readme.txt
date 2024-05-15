1 Configurar o Broker MQTT:

Escolha um servidor MQTT para atuar como broker. Alguns exemplos populares são o Mosquitto e o HiveMQ. Você pode optar por hospedar seu próprio broker ou usar um serviço de hospedagem MQTT na nuvem.

Configure o broker com as credenciais necessárias (endereço IP, porta, nome de usuário, senha, se aplicável).

2 Instalar a biblioteca MQTT no ESP32:

Existem várias bibliotecas MQTT disponíveis para o ESP32. Uma opção comum é a PubSubClient. Você pode instalar esta biblioteca usando o Gerenciador de Bibliotecas do Arduino IDE.

3 Conectar o ESP32 ao Broker MQTT:

Escreva um código para conectar o ESP32 ao broker MQTT. Isso envolve configurar o cliente MQTT com as informações do servidor (endereço IP, porta, credenciais) e estabelecer uma conexão.

4 Publicar mensagens MQTT:

No ESP32, escreva o código para publicar as informações que você deseja enviar para o aplicativo. Essas informações podem ser leituras de sensores, estados de dispositivos, etc.
Use o método publish() da biblioteca MQTT para enviar mensagens para um tópico específico no broker.

5 Desenvolver o Backend do Aplicativo:

No backend do seu aplicativo, você precisará de um serviço ou aplicativo que seja capaz de se inscrever nos tópicos MQTT relevantes para receber as mensagens do ESP32.
Quando o backend recebe as mensagens MQTT, ele pode processá-las conforme necessário e atualizar o estado do aplicativo, enviar notificações aos usuários, etc.
Configurar o Aplicativo:

No lado do aplicativo, você precisará integrar a lógica para se comunicar com o backend e atualizar a interface do usuário conforme as mensagens recebidas do backend.

6 Testar e Depurar:

Teste o sistema completo para garantir que as mensagens estejam sendo enviadas corretamente do ESP32 para o broker MQTT e, em seguida, para o backend do aplicativo. Depure qualquer problema encontrado durante os testes.