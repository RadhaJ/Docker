                   # Docker
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

##STEPS TO CREATE IMAGE:
1.  Launched an Linux instance and login as sudo su administrator<br>
2.  Install docker using below step: yum install docker-io<br>
3.  Start docker using below steps: service docker start<br>
4.  Install git in the instance using below step: yum install git<br>
5.  Cloned my git project url as follows: git clone https://github.com/RadhaJ/Docker<br>
6.  cat Dockerfile<br>
7.  To build the docker image from the docker file: docker build -t webserver<br>
8.  Run docker images to verify that the image was created correctly and that the image name contains a repository that I pushed.ie.web     server docker images<br>
9.  docker run -p 80:80 webserver<br>
10. To create container for the image by running it: docker run -it -d radha/webserver<br>
11. To check the container-id: docker ps -a<br>
12. To execute: docker exec -it bash<br>
13. To have the listener port :80 inside the docker container: apt-get update<br>
14. apt-get install vim<br>
15. cd conf<br>
16. vi server.xml<br>
17. cd webapps<br>
18. rm -r ROOT<br>
19. mv WeatherForecast ROOT<br>
20. exit<br>
21. To commit the docker: docker commit newwebserver:final<br>
22. To save docker images and create .tar file docker save > output.tar<br>
