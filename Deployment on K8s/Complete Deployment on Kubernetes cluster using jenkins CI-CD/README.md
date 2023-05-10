<div align="center">

## Complete Deployment on Kubernetes cluster using jenkins CI-CD

</div>

We will see how jenkins transfer the files, also will see another job of ansible is to run the 
playbook principle so what are the files are going to run here is a `service.yaml` 
file and also a `deployment.yaml` file and kubernetes fetch the latest image 
from the docker registry and based on that it will start building a container 
also we have a service file so that container will be accessible to us using 
the terminal along with the node port we are going to expose 

Select the ansible public ip address and do ssh to the server via putty

Select the webapp-server(k8s cluster) and do `ssh` to the server via `putty`
 
Now we have logged into the 2 servers right one is ansible and left one is webapp-server(k8s cluster)

Set the root password in the webapp(k8s cluster) server

Open sshconfig file we do this to allow network permissions

Enable PermitRootLogin, PasswordAuthentication to yes

Now restart the sshd service 

Generate Public key in the ansible server

Select the ansible public generated key to the webapp server(k8s cluster) enter the password which you previously created

As you can see now we can ssh through other server without need of the password

Go to vi etc-ansible-hosts to add ip of the webserer(k8s cluster) after that save and exit

Ping the server by your group id you created in the host file on ansible server (vi etc-ansible-hosts)

Log back to jenkins

Create an SSH with private key(key pair which you created for the instance)

Copy the generated script

Make a connection bweteen jenkins and directly to the kubernetes server

As you can see, finally the pipeline was successful, I uploaded trouble shoot solutions on reddit

Add the Deployment file to the jenkins-pipeline repo

Add the servicefile to the jenkins-pipeline repo

Add the ansible playbook to the jenkins-pipeline repo

files has been succesful deployed to all the servers pipeline was successful

Add the ansible playbook to run script

Build is successful ansible playbook runing successfully

Lets access the webpage from the nodeport service
