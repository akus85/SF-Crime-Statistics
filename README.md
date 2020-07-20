# SF-Crime-Statistics
SF Crime Statistics with Spark Streaming

## How to use

Start Zookeeper:
`/usr/bin/zookeeper-server-start zookeeper.properties`

Start Kafka-server:
`/usr/bin/kafka-server-start producer.properties`

Put data into topic:
`python kafka_server.py`

Start consumer:
`bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic calls --from-beginning`

Run Spark:
`spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.3.4 --master local[*] data_stream.py`

## Output

### Kafka-console-consumer

![kafka console consumer output](https://github.com/akus85/SF-Crime-Statistics/blob/master/output/kafka-consumer-console.png)


### Spark Job

![spark-job](https://github.com/akus85/SF-Crime-Statistics/blob/master/output/spark-job.png)


### Spark UI

![spark-ui](https://github.com/akus85/SF-Crime-Statistics/blob/master/output/spark-ui.png)