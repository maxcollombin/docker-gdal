# GDAL Docker configuration

This repository contains the configuration files to build a Docker container with GDAL.

The main purpose of this container is to provide a simple way to run GDAL commands without the need to install it on your local machine.

## Start the container

```bash
docker compose up -d
```

## Execute GDAL commands

```bash
docker compose exec gdal ogr2ogr -lco -f PGDump /data/output.sql /data/input.shp
```
or access the container shell

```bash
docker compose exec gdal sh
```
and execute gdal commands

```bash
ogrinfo /data/input.shp
```

## Stop the container

```bash
docker compose down
```