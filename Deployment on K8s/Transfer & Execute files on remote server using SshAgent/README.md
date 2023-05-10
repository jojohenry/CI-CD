<div align="center">

## Transfer & Execute files on remote server using SshAgent
  
</div>

The `SSH protocol` implements agent forwarding, a mechanism whereby an `SSH client` allows an SSH server to use the local `ssh-agent` on the server the user logs into, as if it was local there. When the user uses an SSH client on the server, the client will try to contact the agent implemented by the server, and the server then `forwards` the request to the client that originally contacted the server, which further forwards it to the local agent. This way, ssh-agent and agent forwarding implement single sign-on that can progress transitively.

#### Go to Jenkins and select configure

#### Define new task (stage) block

#### Select SSH agent

#### Select SSH username (private-key)

#### Select ID and description as ansible and username as ubuntu

#### Select the key

#### Copy all the secret

#### Paste the all the data-inside key field and select add

#### Copy the generated pipeline script

#### Paste the generated pipeline script

#### Select the ansible server Public IP


#### Paste the ansible server Public IP in the Groovy script

#### copy the path, this is the path we passing over scp(secure copy) to the ansible


#### Paste the path, in the groovy script as sh(shell script) and <br>click on save and apply


#### Select buildnow it will start the server(script)

#### Sent files to ansible over scp 

#### Now SSH into ansible to check files are replicated or not

#### Files has been copied sucessfully

That's it for this part, happy learning!!

