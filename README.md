# prisma-v1-example

## Setup
```shell
brew tap prisma/prisma
brew install prisma
```

## Run
```shell
docker-compose up -d
```

## BugFix

### No matching manifest for linux/arm64/v8 ...

```shell
ERROR: no matching manifest for linux/arm64/v8 in the manifest list entries
```

* Describe platform to the docker-compose.yaml e.g. `platform: linux/x86_64`

