
Have a look at https://ksqldb.io/quickstart.html

```
docker exec -it ksqldb-cli ksql http://ksqldb-server:8088
```


```
CREATE SOURCE CONNECTOR `jdbc-connector` WITH(
  "connector.class"='io.confluent.connect.jdbc.JdbcSourceConnector',
  "connection.url"='jdbc:postgresql://postgres:5432/postgres',
  "mode"='bulk',
  "connection.password"='password',
  "connection.user"='postgres',
  "topic.prefix"='jdbc-',
  "key"='username');
```

