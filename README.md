# prisma-v1-example

## Setup

```shell
brew tap prisma/prisma
brew install prisma
```

## Set up and connect Prisma with a database

```shell
docker-compose up -d
```

* Prisma running on http://localhost:4466
* Prisma is connected to a local MySQL database (mysql://)
* Currently unprotected
  * Set the `managementApiSecret` property to be protected securely

## Configure Prisma API

```shell
prisma init --endpoint http://localhost:4466
# Create 2 files
```

* `prisma.yml`: Prisma service definition
* `datamodel.prisma`: GraphQL SDL-based datamodel (foundation for database)

## Deploy the Prisma datamodel

```shell
prisma deploy
# model -> ddl
```

## View and edit data from Prisma Admin
* http://localhost:4466/_admin

## Generate the Prisma client


## Documents
* [Prisma V1 docs](https://v1.prisma.io/docs/1.34)
