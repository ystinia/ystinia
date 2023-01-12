# Experiments with SRS Streamer


### Start prepared image

```
docker run --rm -it -p 1935:1935 -p 1985:1985 -p 8080:8080 ossrs/srs:4 ./objs/srs -c conf/docker.conf
```

### Play stream via VLC

```
rtmp://video.server.ip/openipc/openipc
```

### Part of majestic config

```
outgoing:
  - rtmp://video.server.ip:1935/openipc
```
