# SPRING BOOT + APACHE KAFKA

Project that uses Apache Kafka to Exchange Messages Between Producer and Consumer in Spring Boot Applications

### STEP 1 APACHE KAFKA DOWNLOAD
https://www.apache.org/dyn/closer.cgi?path=/kafka/3.7.0/kafka_2.13-3.7.0.tgz

### STEP 2: START THE KAFKA ENVIRONMENT
- Start the ZooKeeper service:

``.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties``

- Start the Kafka broker service:

``.\bin\windows\kafka-server-start.bat .\config\server.properties``

### STEP 3: CREATE A TOPIC TO STORE YOUR EVENTS
``.\bin\windows\kafka-topics.bat --create --topic topic_demo --bootstrap-server localhost:9092``

### STEP 4: WRITE SOME EVENTS INTO THE TOPIC
``.\bin\windows\kafka-console-producer.bat --topic topic_demo --bootstrap-server localhost:9092`` 

``hello world`` 

``topic demo``

### STEP 5:  READ THE EVENTS
``.\bin\windows\kafka-console-consumer.bat --topic topic_demo --from-beginning --bootstrap-server localhost:9092`` 

``hello world``

``topic demo``

# PROJECT RUNNING

Zookeeper and Kafka server runing

![kafka-zookeeper](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/bee0c210-760d-4d96-ba92-90e940580a29)

![kafka-kafka](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/b3cc1014-972c-4e3c-b81a-48f47a843dcf)


Swagger running the publish Json message endpoint

![screenshot (6)](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/4bd53926-0674-4ac3-96f5-ad09486bdc5e)

Kafka Consumer reading the message sent by the endpoint

![kafka-consumer](https://github.com/DaviFarias7/spring-boot-kafka/assets/86566715/db878d74-2b0f-4aaf-8a80-53bc4027d32b)

