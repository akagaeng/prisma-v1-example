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

```shell
prisma generate
# generate files under specified in prisma.yml (./generated/prisma-client)
```

## Setup sample Nodejs application

```javascript
//  index.js
// yarn add prisma-client-lib

node index.js

[
  {
    id: 'cksg78f2j00120839i1gnxjvf',
    name: 'Alice',
    email: 'alice@Wonderland.com'
  }
]
```

## Trouble Shooting
* Apple M1 issues => try from other architecture environment
* Database synchronize is not working properly

```shell
# try delete first, and deploy
prisma delete
prisma deploy
```

## Documents
* [Prisma V1 docs](https://v1.prisma.io/docs/1.34)
