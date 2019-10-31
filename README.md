# ksql_learning

./kafka-topics --list --bootstrap-server localhost:9092  
./kafka-console-consumer --bootstrap-server localhost:9092 --topic <topic_name> --from-beginning  
./kafka-console-consumer --bootstrap-server localhost:9092 --topic <topic_name>  

vi /Confluent/confluent-5.2.1/etc/ksql/ksql-server.properties  
```
listeners=http://localhost:8099
```
./ksql-server-start ../etc/ksql/ksql-server.properties  
./ksql http://localhost:8099 (make sure 8099 port is not taken)  

```CREATE STREAM slow_resp AS
 SELECT * FROM data_filter_dummy_topicname
 WHERE resptime_or_any_column > 250;
 ```
