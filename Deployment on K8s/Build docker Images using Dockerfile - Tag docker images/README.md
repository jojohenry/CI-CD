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

Before we begun make sure you have a Dockerhub account

Select the Jenkins Pipeline

Select configure in the pipeline we created

Build the docker image by adding the stage block 

Apply and save the changes

Trobuleshoot the fail build

Changing into private ip

Error-solved-build-successful and here is the [solution](https://www.reddit.com/user/Mohanse7/comments/y9ocfs/solution_permission_was_denied_while_trying_to/) I posted in reddit 

![6-errors-solved-build-successful-and-solution](https://user-images.githubusercontent.com/58173938/197314956-e587a2cf-9474-43c2-9f9c-3aefc10a37db.png)

Adding Groovy Script for tagging the image

Now apply and save the changes

![9 now apply and save](https://user-images.githubusercontent.com/58173938/197315247-6cd7174d-7636-499f-807e-5541e5cffa3f.png)

### Now its successfull

![10 Now its successfull](https://user-images.githubusercontent.com/58173938/197315272-387f8698-b3c4-45b0-9b91-7033414811fc.png)

### Images has been successful tagged

![11-tag-images-successful](https://user-images.githubusercontent.com/58173938/197315324-8352f690-7231-48f2-a55c-e34a1de891c7.png)
