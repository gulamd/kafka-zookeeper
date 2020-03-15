# kafka-zookeeper

 Each server running one zookeeper node and one kafka node.
 
 In above compose file I have defined the kafka Log Retention Policy configuration. 
 Kafka uses Log data structure to manage its messages
 There are two types of retention policies on kafka.
 1 - Time based retention
 2 - Size based retention
 I have setup these configurations with two environment variables. 
 KAFKA_LOG_RETENTION_HOURS defines the log.retention.hours(time based retention) value and KAFKA_LOG_RETENTION_BYTES defines the log.retention.bytes(size based retention)value
 These fields set on kafka configuration file which locates inside the kafka container(/opt/kafka/config/server.properties).
 
 DEPLOY SERVICES:
 According to your node servers. SSH into all those node and run the below commonad.
 
 # deploy zookeeper1 and kafka1 on service1 --node01
docker-compose up -d zookeeper1
docker-compose up -d kafka1

# deploy zookeeper2 and kafka2 on service2  --node02
docker-compose up -d zookeeper2
docker-compose up -d kafka2

# deploy zookeeper3 and kafka3 on service3 --node03
docker-compose up -d zookeeper3
docker-compose up -d kafka3
