
## Create

```
docker build --no-cache -t nimble:latest .
```

## Start

```
docker run -d --rm --name nimble --hostname nimble -p 0.0.0.0:514:514 -p 0.0.0.0:1935:1935 -p 0.0.0.0:8000:8000 -p 0.0.0.0:8181:8181 nimble
```

## Remove

```
docker rm nimble ; docker rmi nimble ; docker rmi ubuntu:focal
```
