# kafka-mqtt-connector

Docker instance with mqtt connevcor.
Usage:

```
docker run -p 9092:9092 -p 2181:2181  -it -e MQTT_URI=tcp://192.168.0.1:1883 venergiac/kafka-mqtt:latest /bin/bash
```


# test

ON local pc for test

```
$KAFKA_HOME/bin/kafka-console-producer.sh --broker-list localhost:9092 --topic mqtt
```

```
$KAFKA_HOME/bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic mqtt --from-beginning
```
