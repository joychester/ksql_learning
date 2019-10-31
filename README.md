# ksql_learning

./kafka-topics --list --bootstrap-server localhost:9092
./kafka-console-consumer --bootstrap-server localhost:9092 --topic <topic_name> --from-beginning
./kafka-console-consumer --bootstrap-server localhost:9092 --topic <topic_name>

./ksql-server-start ../etc/ksql/ksql-server.properties
./ksql http://localhost:8099

```CREATE STREAM slow_resp AS
 SELECT * FROM date_filter
 WHERE resptime > 250;
