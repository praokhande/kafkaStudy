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

Publish data from csv file:
c:\kafka_2.13-3.6.1>bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic prabhakar-topic <C:\Work\kafkaStudy\users.csv

************************************************************************************************************************************
Start confluent kafka zookeeper:
c:\Work\programs\confluent-7.6.0>bin\windows\zookeeper-server-start.bat etc\kafka\zookeeper.properties

Start confluent kafka server:
c:\Work\programs\confluent-7.6.0>bin\windows\kafka-server-start.bat etc\kafka\server.properties

Create Topic:
c:\Work\programs\confluent-7.6.0>bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --create --topic NewTopic1 --partitions 3 --replication-factor 1

list out all topics:
bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --list --topic NewTopic1

bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --describe --topic NewTopic1

produce message:
bin\windows\kafka-console-producer --broker-list localhost:9092 --topic NewTopic1

consume message:
bin\windows\kafka-console-consumer --bootstrap-server localhost:9092 --topic NewTopic1 --from-beginning

Send CVS file data to kafka:
bin\windows\kafka-console-producer --broker-list localhost:9092 --topic NewTopic1 <C:\Work\kafkaStudy\users.csv

************************************************************************************************************************************
Start Kafka without zookeeper: kraft: https://kafka.apache.org/quickstart


