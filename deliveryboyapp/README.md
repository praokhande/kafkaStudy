kafka commands:

Start Zookeeper:
C:\kafka_2.13-3.6.1>bin\windows\zookeeper-server-start.bat config\zookeeper.properties

Start Kafka Server:
C:\kafka_2.13-3.6.1>bin\windows\kafka-server-start.bat config\server.properties

create a topic:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-topics.bat --create --topic user-topic --bootstrap-server localhost:9092

Check available topics:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092


Kafka console producer:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-console-producer.bat --topic user-topic --bootstrap-server localhost:9092
>hi
>this is my message

Kafka console consumer:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-console-consumer.bat --topic user-topic --from-beginning --bootstrap-server localhost:9092
hi
this is my message
