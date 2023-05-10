<div align="center">

# Dockerfile - Configure Webhook - Trigger Jenkins Job - git

</div>

In a typical CI/CD pipeline, what happens is when you push your code to a `code repository (remote)` 
like `GitHub/GitLab/BitBucket`, an event is triggered by the git host provider. This trigger is 
known as `WebHook`. This webhook can be used by some third-party services to provide an array of integrations.

Here the performed task is to run a build that creates a docker image and pushes it to `Docker Hub Registry`. 
From there one can pull the images to further use them for further consumption. This image is consumed by `Kubernetes cluster`


### Create a [Dockerfile](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/blob/main/Dockerfile%20-%20Configure%20Webhook%20-%20Trigger%20Jenkins%20Job%20-%20git/Dockerfile/Dockerfile)

And push the Dockerfile to a separate [Repository](https://github.com/Krishnamohan-Yerrabilli/jenkins-pipeline)

### Why we need separate repo

#### Because it makes it easy to Jenkins to fetch the file(more on this later)

![1-Dockerfile](https://user-images.githubusercontent.com/58173938/196869950-4b9bee5c-885e-456b-8ed1-c0ab2a8b67a4.png)

#### Now login into your Jenkins account

![2-jenkins-login](https://user-images.githubusercontent.com/58173938/196870673-f1b72fa9-64a4-48d1-a6ae-1a1b2cbfb7c9.png)

#### Creating a pipeline, click on the new item


#### Select the pipeline 


#### Enter youre repo name 


#### We're writing a script using groovy 


#### Build is successfully 


#### What we have done until now is a manual process, let's automate this stuff. select configure gitSCM


#### Configure web hook


#### To provide the `API token`(one type of secret), go to Jenkins

*Copy the API token and paste this into the GitHub webhook. secret field*

#### Save the stuff

#### Reload (You will get a successful checkmark) to sync 


#### Now let's make a change in Dockerfile and push it to the separate repo we created, 
*This is the link we paste in Jenkins script*

#### woohoo we successfully triggered the Jenkins, by committing a new change in the Dockerfile via GitHub


