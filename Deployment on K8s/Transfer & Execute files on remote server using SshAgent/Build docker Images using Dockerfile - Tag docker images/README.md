<div align="center">

# Build docker Images using Dockerfile - Tag docker images

</div>

Were going to build the image based on the docker file along with the tag it's important 
to track images aka (version maintaining)will have a job based on the build number 
it will have a tag with the image we will use the pipeline job name along with 
that we will have the build number so how many times we are running the pipeline 
you will get the number `jenkins-pipeline:1.1` `jenkins-pipeline:1.2` 

This is what we get along with that, for each and every `tag 1.3` also you will get a 
latest image for `tag 1.4` also you will get the latest image and so on, while we going 
through that process we are maintaining a version of the image so that at any 
point of time we can do roll back, let's hop into it.

### Before we begun make sure you have a Dockerhub account

### Select our Jenkins Pipeline

### Select configure in the pipeline we created

### Build the docker image by adding the stage block 

### Apply and save the changes

### Trobuleshoot the fail build

### Changing into private ip

### Error-solved-build-successful

### Wohoo we successfully build the image

### Adding Groovy Script for tagging the image

### Now apply and save the changes

### Now its successfull

### Images has been successful tagged

That's it for this part, happy learning!!
