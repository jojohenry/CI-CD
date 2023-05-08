<div align="center">

## Deployment on Kubernetes Cluster using Jenkins CI/CD Project

![completecicd](https://user-images.githubusercontent.com/109822667/234435363-3324cf3c-f48c-40cb-b389-cc0a6d8546ff.png)

[*Project Source*](https://www.udemy.com/course/valaxy-devops/)

### This Repo is to Teach You Each Tool/Technology and How to Implement the Whole Project Step by Step 

</div>

## Prerequisites/tools needed to work on this project. 
 
- [AWS EC2](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)
- [Containers](https://www.redhat.com/en/topics/containers/whats-a-linux-container)
- [Docker](https://docs.docker.com/get-started/overview/)
- [Kubernetes](https://kubernetes.io/)
- [Jenkins](https://www.jenkins.io/doc/tutorials/)
- [Ansible](https://docs.ansible.com/ansible/latest/getting_started/index.html)

In this project, you will learn how to utilize a wide range of DevOps tools including GitHub, Jenkins, <br> Ansible, and a `Kubernetes cluster(2 nodes)` using `Jenkins CI/CD pipeline`. <br>

Additionally, you will be gaining knowledge about Kubernetes services and deployment methods, <br> and writing `Ansible playbooks` and `Dockerfiles` to support our deployment.

## Agenda 

 - When a developer writes a Docker file, they will push it to the corresponding `GitHub repository`. <br> Whenever there is a new commit to the repository, Jenkins will be notified via a webhook, and <br> the pipeline will be initiated accordingly.

 - When Jenkins receives a notification from GitHub about new changes, it will fetch all the
  updated <br> code from the repository. When this is completed, Jenkins will establish an SSH connection with <br> Ansible server. This enables the server to access the Dockerfile `pushed` by the developer and <br> subsequently execute  the container image.

 - When it gets the docker file it will intitate the process of building the container image based on the <br> docker file. Once the image is successfully built, Jenkins will
  `tag` it, and push it to the Docker Hub. <br> Meanwhile, the Ansible
  server will perform its second task by establishing an SSH connection <br> with the Kubernetes cluster server. The cluster server will then review the playbook and Ansible will <br> execute it accordingly.

 - Using the `kubectl` command, the Kubernetes cluster running our web application will attempt to <br> fetch the
  latest container image from the Docker registry. Once the image is retrieved, the cluster <br> will start
  building the image and container, and that container can be accessed using the <br> specified `node IP` and `port` as indicated in the `Service.yaml`.
  

 - To intitiate the Kubernetes deployment, you will start by writing the `Service.yaml` file and transfer it <br> the Kubernetes cluster. This is a key component in acheiving the successful `Kubernetes web deployment`

 - To enable Jenkins CI/CD pipeline, we will need to leverage various tools, including `Linux` commands, <br> Jenkins, and Docker. Additionally, you would need a `Dockerhub account`, in order to push the Docker <br> image built by the `Ansible Server` <br> to the Docker Hub.

 - To ensure that you have access to the most up-to-date image, you must log in to our Docker Hub account. <br> By doing so, you can easily push the latest image to the Docker Hub, while simultaneously maintaining <br> a version based on the build.

 - For instance, if you build v1, this will contain a fresh image. Subsequently, if we build a second image (v2), <br> this will contain the `latest image`. It is important that you seperate the latest image from previous builds.<br>

## Project Steps

- [Step One - Server Setup](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Server%20Setup) 
- [Step Two - Dockerfile - Configure Webhook - Trigger Jenkins Job - git](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Dockerfile%20-%20Configure%20Webhook%20-%20Trigger%20Jenkins%20Job%20-%20git) 
- [Step Three - Transfer & Execute files on remote server using SshAgent](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Transfer%20%26%20Execute%20files%20on%20remote%20server%20using%20SshAgent)
- [Step Four - Build docker Images using Dockerfile - Tag docker images](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Build%20docker%20Images%20using%20Dockerfile%20-%20Tag%20docker%20images)
- [Step Five - Complete Declarative CI/CD Pipelines in Jenkins Project - Push Images to DockerHub](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Complete%20Declarative%20CI-CD%20Pipelines%20in%20Jenkins%20Project%20-%20Push%20Images%20to%20DockerHub)
- [Step Six - Complete Deployment on Kubernetes cluster using jenkins CI/CD](https://github.com/Krishnamohan-Yerrabilli/Deployment-on-K8s-cluster-using-jenkins-CI-CD/tree/main/Complete%20Deployment%20on%20Kubernetes%20cluster%20using%20jenkins%20CI-CD)

