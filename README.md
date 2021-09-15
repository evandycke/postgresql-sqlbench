# PostgreSQL & sqlbench

Discover and test sqlbench.

[![forthebadge](https://forthebadge.com/images/badges/you-didnt-ask-for-this.svg)](http://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/contains-technical-debt.svg)](http://forthebadge.com)  [![forthebadge](https://forthebadge.com/images/badges/check-it-out.svg)](http://forthebadge.com)  [![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](http://forthebadge.com)

![PostgreSQL](./images/postgresql-logo-256.png)

## Getting started with SqlBench

* Clone this project
* Use docker-compose and the docker-compose.yaml file

```bat
docker-compose up -d
```

* Install Go
* Install Sqlbench with Go

```go
go get -u github.com/felixge/sqlbench
```

* Call Sqlbench in CL

```bat
sqlbench -c postgres://admin:password@localhost:5432/adventureworks?sslmode=disable -n 1000 -p -v -m client -o baseline.csv scripts/unqualified.sql scripts/qualified.sql scripts/ordered.sql
```

The result of this command is :

![sqlbench result](./images/result.png)


* Use docker-compose to stop properly the project

```bat
docker-compose down
```

## Useful links

* [SqlBench](https://github.com/felixge/sqlbench) - Tool to measures and compares the execution time of SQL queries on PG database

## Build with

* [PostgreSQL](https://www.postgresql.org) - Open source object-relational database system
* [Docker](https://www.docker.com/) - Set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers
* [Git](https://git-scm.com) - Open source distributed version control system
* [pgAdmin](https://www.pgadmin.org/) - Open Source administration and development platform for PostgreSQL
* [Go](https://golang.org/) - Open source programming language 

## Contributing

If you would like to contribute, read the CONTRIBUTING.md file to learn how to do so.
