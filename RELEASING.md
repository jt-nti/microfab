# Release process

Releasing new versions of Hyperledgendary fork of microfab is currently a manual process.

## Create GitHub release 

Create a new [microfab fork release](https://github.com/hyperledgendary/microfab/releases) 

## Publish Docker image

Publish a docker image by following the instructions for [Pushing a Docker container image to Docker Hub](https://docs.docker.com/docker-hub/repos/#pushing-a-docker-container-image-to-docker-hub), e.g.

```
docker build --no-cache -t hyperledgendary/microfab .
docker tag hyperledgendary/microfab hyperledgendary/microfab:tag
docker push hyperledgendary/microfab
docker push hyperledgendary/microfab:tag
```
