# Viewing Documentation 

## database

1. clone this repo
2. open `doc/db/index.html`
3. you can also view the documentation with [htmlpreview](https://htmlpreview.github.io/?https://github.com/thematters/developer-resource/blob/master/doc/db/index.html), but diagram needs to be viewed [either locally or on GitHub](./db/diagram/summary/relationships.real.compact.svg)

# Generating Documentation 

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
