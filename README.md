# SPRING BOOT + APACHE KAFKA

Projeto que utiliza Apache Kafka para trocar mensagens entre Produtor e Consumidor em aplicações Spring Boot.

### PASSO 1: DOWNLOAD DO APACHE KAFKA 
https://www.apache.org/dyn/closer.cgi?path=/kafka/3.7.0/kafka_2.13-3.7.0.tgz

### PASSO 2: INICIE O AMBIENTE DO KAFKA
- Inicie o service do ZooKeeper:

``.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties``

- Inicie o broker do servidor Kafka:

``.\bin\windows\kafka-server-start.bat .\config\server.properties``

### PASSO 3: CRIE UM TÓPICO PARA GUARDAR SEUS EVENTOS
``.\bin\windows\kafka-topics.bat --create --topic topic_demo --bootstrap-server localhost:9092``

### PASSO 4: ESCREVA ALGUNS EVENTOS NESTES TÓPICO
``.\bin\windows\kafka-console-producer.bat --topic topic_demo --bootstrap-server localhost:9092`` 

``hello world`` 

``topic demo``

### PASSO 5:  LEIA OS EVENTOS
``.\bin\windows\kafka-console-consumer.bat --topic topic_demo --from-beginning --bootstrap-server localhost:9092`` 

``hello world``

``topic demo``

# EXECUTANDO O PROJETO

Zookeeper e servidor Kafka server em execução:

![kafka-zookeeper](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/bee0c210-760d-4d96-ba92-90e940580a29)

![kafka-kafka](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/b3cc1014-972c-4e3c-b81a-48f47a843dcf)


Swagger executando o endpoint que publica a mensagem Json

![screenshot (6)](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/4bd53926-0674-4ac3-96f5-ad09486bdc5e)

Kafka Consumer lendo as mensagens enviadas pelo endpoint

![kafka-consumer](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/db878d74-2b0f-4aaf-8a80-53bc4027d32b)

