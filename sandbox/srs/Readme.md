# Experiments with SRS Streamer


### Start prepared SRS image

```
docker run --rm -it -p 1935:1935 -p 1985:1985 -p 8080:8080 ossrs/srs:5
```

### Part of majestic config

```
outgoing:
  enabled: true
  server: rtmp://172.19.32.17:1935/live/openipc-19-178
```

### Play stream via MPV

```
rtmp://172.19.32.17/live/openipc-19-178
```
