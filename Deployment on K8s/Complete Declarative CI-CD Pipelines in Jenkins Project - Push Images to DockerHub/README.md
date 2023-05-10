<div align="center">

# Complete Declarative CI-CD Pipelines in Jenkins Project - Push Images to DockerHub

 
</div>

I already stated we need to have a Dockerhub account, so once ansible Server builds a 
Docker image based on the Docker file, we push it to Docker Hub. So we need to log in to 
`DockerHub`, therfore we can easily push the latest image what we're trying to accomplish 
here is we have the latest image and we also maintain a version based on the build
It builds v1, it contains a fresh image

If the second time it builds another `image v2`, so that the second one contains the latest 
image, we're also maintaining `version control`, cause we also see how to separate the latest image 
from tagged images.

Log back to the jenkins server

Password is not good, we use creditails Plugin

Secret text for password plugin

Provide your secret

Copy the generated password

Password is created, now were gone push images to the docker registry

We docker push script sh intiated

Save and apply 

Copy the Public ip to ssh to the server

Enter your dockerhub crenditails for authentication purposes

Select buildnow to do all the work that we assigned to the jenkins

Image has been successfully pushed to docker hub






