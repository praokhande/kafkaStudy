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

Start Zookeeper:
C:\Work\kafka_2.13-3.6.1>bin\windows\zookeeper-server-start.bat config\zookeeper.properties
port: 2181

Start Kafka server/boker:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-server-start.bat config\server.properties
port: 9092

Tocreate kafka Topic:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --create --topic prabhakar-topic --partitions 3 --replication-factor 1
Created topic prabhakar-topic.

Check all topics:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --list
__consumer_offsets
location-update-topic
prabhakar-topic
prabhakar-topic1
user-topic

C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --describe --topic prabhakar-topic
Topic: prabhakar-topic  TopicId: wJMuxO1MRlOoqQkDQRXJDg PartitionCount: 3       ReplicationFactor: 1    Configs:
Topic: prabhakar-topic  Partition: 0    Leader: 0       Replicas: 0     Isr: 0
Topic: prabhakar-topic  Partition: 1    Leader: 0       Replicas: 0     Isr: 0
Topic: prabhakar-topic  Partition: 2    Leader: 0       Replicas: 0     Isr: 0


Start Console Publisher:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic prabhakar-topic

Start Console Consumer:
C:\Work\kafka_2.13-3.6.1>bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic prabhakar-topic --from-beginning
