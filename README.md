                   # Project-1
Migrating Weather Forecaster into a docker container instance

Docker container instance acts as a more portable and modular framework for hosting services.<br>
Docker provides a stand-alone Linux environment where you can install your libraries and run your applications within an isolated environment.<br>

##STEPS TO RUN MY IMAGE:
https://drive.google.com/open?id=0Bz8NPDzUMpEwM0xDczZwSDBZeEk
<br>
<b>download jarubula.tar from the above link</b>
<br>
1.	Install the docker in aws environment.<br> 
Install (as root): yum install docker-io <br>
Start the docker service (as root): service docker start<br>
2.	Docker load -i jarubula.tar<br>
3.	//new image will be created and displays the image-id.<br>
4.	Copy the newly created image-id(visible below the docker load command).<br>
5.	Docker run -d -p 8081:80 (copied id) <br>
6.	Check in the browser with your instance ip(ip:8081/).<br>
