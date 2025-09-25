## Start Apache Kafka

### 1 Start zookeeper
```
bin/zookeeper-server-start.sh config/zookeeper.properties
```

### 2 Start kafka server
```
bin/kafka-server-start.sh config/server.properties
```

### 3 Create topic messages
```
bin/kafka-topics.sh --create --topic EVENT_MESSAGES --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
```

### 4 Listen message
```
bin/kafka-console-consumer.sh --topic EVENT_MESSAGES --from-beginning --bootstrap-server localhost:9092
```
