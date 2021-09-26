# Run Apache Kafka
## Start the Kafka cluster
Run the following command to start ZooKeeper:
```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
```
There will be a lot of output, and ZooKeeper will be ready in a short time, typically around a second or two.

Open another terminal session. Change the directory to the kafka directory, and start the Kafka broker:
```bash
cd kafka_2.12-2.6.0
bin/kafka-server-start.sh config/server.properties
```

