# Apache Kafka Installation (Single-node) — Step-by-step

## Download & extract
```bash
wget https://downloads.apache.org/kafka/3.5.0/kafka_2.13-3.5.0.tgz
tar -xvf kafka_2.13-3.5.0.tgz
cd kafka_2.13-3.5.0
```

## Start Zookeeper & Kafka
```bash
bin/zookeeper-server-start.sh config/zookeeper.properties &
bin/kafka-server-start.sh config/server.properties &
```

## Create topic & test
```bash
bin/kafka-topics.sh --create --topic test --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
bin/kafka-console-producer.sh --topic test --bootstrap-server localhost:9092
bin/kafka-console-consumer.sh --topic test --from-beginning --bootstrap-server localhost:9092
```

## Tips
- Use systemd services for production and separate nodes for brokers.
