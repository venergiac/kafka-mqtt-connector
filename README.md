# kafka-mqtt-connector

Docker instance with mqtt connevcor.
Usage:

```
docker run -p 9092:9092 -p 2181:2181  -it -e MQTT_URI=tcp://$EXTERNAL_IP:1883 -e KAFKA_ADVERTISED_HOST_NAME=$EXTERNAL_IP venergiac/kafka-mqtt:latest /bin/bash
```


# interactive


```
docker run -it -p 9092:9092 -p 2181:2181  -e MQTT_URI=tcp://192.168.0.1:1883 venergiac/kafka-mqtt /bin/bash
```

# test

ON local pc for test

```
$KAFKA_HOME/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic mqtt
```

```
$KAFKA_HOME/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic mqtt --from-beginning
```


$KAFKA_HOME/bin/kafka-console-producer.sh  --broker-list 10.79.101.235:9092 --topic mqtt


$KAFKA_HOME/bin/kafka-console-consumer.sh --zookeeper 10.79.101.235:2181 --bootstrap-server 10.79.101.235:9092 --topic mqtt --from-beginning