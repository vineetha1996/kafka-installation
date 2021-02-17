# kafka-installation

## Commands used:

 Open PowerShell in C:\kafka_2.13-2.7.0 (path where i installed kafka)

 I used different PowerShell window for each process.

 Window 1 - Run Zookeeper Service 
```
.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
```
Window 2 - Run Kafka Service
```
.\bin\windows\kafka-server-start.bat .\config\server.properties
```
Window 3 Execute One-Time Commands to create, list, delete topic
```
.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic Favorite-Novels

.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list
```
Window 4 - Run Kafka Producer 
```
.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic Favorite-Novels
```
Give your inputs in the powershell

Window 5 - Run Kafka Consumer - To show the given inputs from the begining
```
.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic Favorite-Novels --from-beginning
```
You can see the inputs given in the producer window
