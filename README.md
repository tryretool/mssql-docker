# mssql-docker
Spin up an Microsoft SQL Server DB with the [Northwinds sample dataset](https://github.com/Microsoft/sql-server-samples/tree/master/samples/databases/northwind-pubs) for local testing via Docker Desktop

1) Set the [tag](https://hub.docker.com/_/microsoft-mssql-server) you want to use in `database.Dockerfile`

2) `docker compose up -d --build`

3) Create a new mssql resource:
    ````
    host: host.docker.internal
    port: 1433
    username: sa
    pw: (see SA_PASSWORD in compose.yml)
    ````

4) Outside of Retool, use a SQL GUI like [TablePlus](https://tableplus.com/) to connect to the database to inspect data/run queries
