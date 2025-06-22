# Docker-Tutorial
All required  docker concept for data scientist/MLops nitish sir(CampusX)
## What is docker??
Docker is a software platform that allows you to build, test, and deploy applications quickly using containers.

## Why use Docker??

- In general multiple websites are hosted on single server then let say one website gets hacked and some hacker reached to our website as well then this may be a problem.

- Another problem is suppose 1 website starts demanding higher resource leading to lack of resource & which may further lead to performance issue.
- Also in general we host our website in multiple servers & since our application is in container form then we can quickly send the copy of container to accross different server and run our application(horizontal scaling).When needed we again remove them from different server.
- such isolations are offer efficiently by Docker.
- We can use virtual machines but they are very heavy as they also carry OS in return docker is very light weight.
- ![image](https://github.com/user-attachments/assets/5663409d-c818-4398-8b67-4529f1b0aeac)

## Terminologies
![image](https://github.com/user-attachments/assets/a7820613-758a-411a-9554-2d6302b9abd8)
![image](https://github.com/user-attachments/assets/31496e84-6089-4315-a8bf-3fc61db4f46e)
### Docker Image(Container/Dabba):
(for now ignore the term like docker file,docker registry,etc.. )
- Life cycle
- 1.Docker image is created 1st
- Then image is stored
- from there people downloads the image
- And then developers runs it.
![image](https://github.com/user-attachments/assets/1504251c-8b21-48db-83ab-8022452c0468)

![image](https://github.com/user-attachments/assets/e3ecccbe-6ffd-495a-b1b4-5ec7d1e644b6)
![image](https://github.com/user-attachments/assets/813cef05-cc66-489c-be15-22ec387a12ca)

eg:
![image](https://github.com/user-attachments/assets/d3eb95e4-a14e-4f49-8087-cc7024b4478a)
### Docker Container
See image(daaba kisi machine me jab chalta hai toh uska 1 instance create hota hai u& sse hi docker container bolte hai.)
![image](https://github.com/user-attachments/assets/797f1959-b1c5-4257-9b13-770abbcc6a48)
### Docker Registry
-Docker images are stored here & user/tester can download that image from here.
![image](https://github.com/user-attachments/assets/6b3b0e1a-653b-4a0a-a8d6-9ed840a263fe)
#### Registry's benifits
![image](https://github.com/user-attachments/assets/8ea3aa15-bc28-4476-b1c6-7a5c78c8df17)


### Docker Lifecycle:
![image](https://github.com/user-attachments/assets/3be049de-9e3d-4fb2-8b58-4b62c69353d8)


Video link:https://youtu.be/GToyQTGDOS4?si=cGNuXO-N7nEgPTcC
(left:35:39)

