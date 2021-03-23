# DockerOnAWS

## Initializing

// first build your docker to an image
$ docker build -t AppName

// get id of your built image

$ docker image ls

// log to AWS using credentials or tokens

$ docker login -u AWS -p $(aws ecr get-login-password --region the-region-you-are-in) xxxxxxxxx.dkr.ecr.the-region-you-are-in.amazonaws.com

// Add tags

$ docker tag 55ea89f42d75  xxxxxxxxxxxx.dkr.ecr.eu-north-1.amazonaws.com/myapp-name

// push to AWS ECR 

$ docker push xxxxxxxxxxxx.dkr.ecr.eu-north-1.amazonaws.com/myapp-name

// then follow the instruction for Amazon services


