# hardware/selfoss

![selfoss](https://i.imgur.com/8hJyBgk.png "selfoss")

### What is this ?

The new multipurpose rss reader, live stream, mashup, aggregation web application.

### Features

- Lightweight & secure image (no root process)
- Based on Alpine Linux
- Latest Selfoss version (2.17)
- SQLite driver
- With Nginx and PHP7

### Build-time variables

- **VERSION** = selfoss version (default: **2.17**)
- **SHA256_HASH** = SHA256 hash of selfoss archive

### Ports

- 8888

### Environment variables

| Variable | Description | Type | Default value |
| -------- | ----------- | ---- | ------------- |
| **UID** | selfoss user id | *optional* | 991
| **GID** | selfoss group id | *optional* | 991
| **CRON_PERIOD** | Cronjob period for updating feeds | *optional* | 15m

### Reverse proxy

https://github.com/Wonderfall/dockerfiles/tree/master/boring-nginx

### Docker-compose

#### Docker-compose.yml

```
selfoss:
  image: hardware/selfoss
  container_name: selfoss
  volumes:
    - /mnt/docker/selfoss:/selfoss/data
```

#### Run !

```
docker-compose up -d
```
