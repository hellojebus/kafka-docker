Start up Docker Images

`docker-compose up`

1. Connect to Kafka Container via Bash

`docker exec -it {container_name} bash`

2. Create a topic

`kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic test`

3. Create Producer

`kafka-console-producer.sh --broker-list localhost:9092 --topic test`

4. Create Consumer (One second terminal)

`kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test`

5. Go back to Producer terminal, and enter your first message. It will show up in the consumer terminal! 
