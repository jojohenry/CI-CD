<div align="center">

## Deployment on Kubernetes Cluster using Jenkins CI/CD Project

![completecicd](https://user-images.githubusercontent.com/109822667/234435363-3324cf3c-f48c-40cb-b389-cc0a6d8546ff.png)

</div>

[*Project Source*](https://www.udemy.com/course/valaxy-devops/)

<div align="center">

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

 - When a developer writes a Dockerfile, they will push it to the corresponding `GitHub repository`. <br> Whenever there is a new commit to the repository, Jenkins will be notified via a webhook, and <br> the pipeline will be initiated accordingly.

 - When Jenkins receives a notification from GitHub about new changes, it will fetch all the
  updated <br> code from the repository. When this is completed, Jenkins will establish an SSH connection with <br> Ansible server. This enables the server to access the Dockerfile `pushed` by the developer and <br> subsequently execute  the container image.

 - When it gets the Dockerfile it will intitate the process of building the container image based on <br> the Dockerfile. Once the image is successfully built, Jenkins will
  `tag` it, and push it to DockerHub. <br> Meanwhile, the Ansible
  server will perform its second task by establishing a SSH connection <br> with the Kubernetes cluster server. The cluster server will then review the playbook and Ansible <br> will execute it accordingly.

 - Using the `kubectl` command, the Kubernetes cluster running the web application will attempt to <br> fetch the
  latest container image from the Docker registry. Once the image is retrieved, the cluster <br> will start
  building the image and container, and that container can be accessed using the specified <br> `node IP` and `port` as indicated in the `Service.yaml`.
  
 - To intitiate the Kubernetes deployment, they will start by writing the `Service.yaml` file and transfer <br> it to the Kubernetes cluster. This is a key component in acheiving the successful `Kubernetes web` <br> `deployment`

 - To enable Jenkins CI/CD pipeline, they will need to leverage various tools, including `Linux` commands, <br> Jenkins, and Docker. Additionally, they will need a `Docker hub account`, in order to push the Docker <br> image built by the `Ansible Server` to the Docker Hub.

 - To ensure that they have access to the most up-to-date image, they must log in to the Docker Hub <br> account. By doing so, they can easily push the latest image to Docker Hub, while simultaneously  <br> maintaining a version based on the build.

 - For instance, if you build v1, this will contain a fresh image. Subsequently, if you build a second image <br> (v2), `preforming a version`.It is important that you seperate the `latest image` from previous builds.<br>

## Project Steps

- [Step One - Server Setup](https://github.com/jojohenry/CI-CD/tree/main/Deployment%20on%20K8s/Server%20Setup) 
- [Step Two - Using Dockerfile to Configure Webhook and Trigger Jenkins Job](https://github.com/jojohenry/CI-CD/tree/main/Deployment%20on%20K8s/Dockerfile%20-%20Configure%20Webhook%20-%20Trigger%20Jenkins%20Job) 
- [Step Three - Transfer & Execute Files on Remote Server using SSHAgent](https://github.com/jojohenry/CI-CD/tree/main/Deployment%20on%20K8s/Transfer%20%26%20Execute%20files%20on%20remote%20server%20using%20SshAgent)
- [Step Four - Building Docker Images using Dockerfile and Tagging Docker Images](https://github.com/jojohenry/CI-CD/tree/main/Deployment%20on%20K8s/Build%20docker%20Images%20using%20Dockerfile%20-%20Tag%20docker%20images)
- [Step Five - Complete Declarative CI/CD Pipeline in Jenkins and Pushing Image to Docker Hub](https://github.com/jojohenry/CI-CD/tree/main/Deployment%20on%20K8s/Complete%20Declarative%20CI-CD%20Pipelines%20in%20Jenkins%20Project%20-%20Push%20Images%20to%20DockerHub)
- [Step Six - Complete Deployment on Kubernetes Cluster using Jenkins CI/CD](https://github.com/jojohenry/CI-CD/tree/main/Deployment%20on%20K8s/Complete%20Deployment%20on%20Kubernetes%20cluster%20using%20jenkins%20CI-CD)

