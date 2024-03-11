# MSSQL Docker
A way to Run MS SQL locally using docker

## Prerequisites

- [Docker Installed](https://www.docker.com/products/docker-desktop/)

## Get the server up and running

```bash
docker-compose up -d
```

## Get Backup into container

1) Make sure file is readable `chmod 666 <filename>`

2) Copy file into Docker`docker cp <filename> <containerid>:/var/opt/mssql/backup/<filename>`

    example:

    ```bash
    docker cp db.bak 29027d325b9012ae0517c3bbc6fd7e25f4daaedf6acf4806bfd41afa1e71a762:/var/opt/mssql/backup/db.bak
    ```

3) Use Azure data studio or similar to restore DB.
