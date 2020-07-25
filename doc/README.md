# Documentation generation

## database

1. Install [Java](https://java.com/en/download/manual.jsp), [PostgreSQL JDBC driver](https://jdbc.postgresql.org/download.html) and [SchemaSpy](http://schemaspy.org/).
2. For example for SchemaSpy 6.1.0 and JDBC driver 42.2.14, write documentation to `db` folder with

```
java -jar schemaspy-6.1.0.jar -t pgsql \
  -s public -db [database name] -u [user name] -p [password] \
  -host [host address] -o db \
  -dp ./postgresql-42.2.14.jar \
  -vizjs -renderer :cairo -norows
```
