# Experiments with Nimble Streamer


### Create image

`docker build --no-cache -t nimble:latest .`

### Start container

`docker run -d --rm --name nimble --hostname nimble -p 0.0.0.0:554:554 -p 0.0.0.0:1935:1935 -p 0.0.0.0:8000:8000 -p 0.0.0.0:8181:8181 nimble`

### Stop and Remove container

`docker stop nimble`

`docker rm nimble  # If there are errors in the work`

### Remove images

`docker rmi nimble`

`docker rmi ubuntu:focal`
