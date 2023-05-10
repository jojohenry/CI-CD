<div align="center">

## Pre-Setup

</div>


Provision `3 EC2 instances` For this project purpose, set security groups to allow all incoming traffic, for all 3 instances Setup `2 instances` for Jenkins(Jenkins-server) and ansible(Ansible-server) (use `t2.micro`) for both instances, give `volume 10GB` per instance `Setup 1 instance` for (Webapp-server)k8s cluster (use `t2.medium`) 25GB for the instance For this project purpose, `set security groups to allow all incoming traffic`
<br>

If you're facing any difficulty to ssh, checkout my trobuleshooting [guide](https://www.reddit.com/user/Mohanse7/comments/y7uu26/troubleshootingfixing_ssm_agent_how_to_perform/)

Install putty on you're local machine or on you're type2 hypervisor


After sucessfull installation type `putty` in the respected fiels, enter putty in search bar <br>
or enter putty in you're terminal
<br />


Before you copy your instance Public Ip address, make sure you download `.ppk` key-pair 
 
select the respective Instance public Ip address 
 
Choose between raw, Telnet, rlogin, SSH, or serial connection. Enter a port number, <br>
a server hostname or IP address, and start a new session, for this context choose SSH
  
Paste in to the putty `hostname or Ipaddress` field, Select your `.ppk` and choose open

After you open select a pop up will rise, select `Approve` and and now you would see <br>
`login:` in most of the cases the username will be `ubuntu`, 

Next step:

login to each ec2 instance via putty and run the selected EC2 shell script files 


I hope you learn something new, happy learning!!


 
