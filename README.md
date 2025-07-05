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
![image](https://github.com/user-attachments/assets/eb7545fd-b80d-462a-9735-5cdd88b55b84)
![image](https://github.com/user-attachments/assets/3166b153-bb96-4a7c-a556-e955d9a55b08)

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

## Use Cases:

### Microservices Architecture

Description: Microservices break down applications into smaller, independent services,

each running in its own container.

#### Benefits:
Simplifies deployment, scaling, and maintenance. Each service can be

developed, updated, and deployed independently.


### Continuous Integration and Continuous Deployment (CI/CD)
Description: Docker ensures a consistent environment from development through testing

to production.

#### Benefits: 
Streamlines the CI/CD pipeline, reduces discrepancies between environments,

and speeds up testing and deployment processes.


### Cloud Migration

• Description: Containerizing applications to move them to the cloud.

#### Benefits:
Simplifies the migration process, allows applications to run consistently across

different cloud providers, and optimizes resource usage.


### Scalable Web Applications

• Description: Deploying web applications in containers for easy scaling.

Benefits: Simplifies scaling up or down based on traffic, ensures consistent deployment,

and enhances resource utilization.


### Testing and QA

• Description: Creating consistent environments for testing applications.

Benefits: Ensures tests are run in environments identical to production, speeds up the

setup of test environments, and facilitates automated testing.


### Machine Learning and AI

• Description: Deploying machine learning models and AI applications in containers.

Benefits: Ensures consistency in the runtime environment, simplifies scaling of model

training and inference, and facilitates collaboration and reproducibility.


### API Development and Deployment

• Description: Developing and deploying APIs in containers.

Benefits: Ensures APIs run consistently across environments, simplifies scaling, and

improves deployment speed and reliability.


![image](https://github.com/user-attachments/assets/b7aa1feb-bf22-4816-bf75-a4fcd897f958)
## Pulling docker image to our Machine
go to docker hub>search image >copy the command(similar to docker pull hello-world) > paste inside docker dekstop terminal.

### Pulling streamlit application inside docker dekstop
go to docker hub>search image >copy the command(similar to docker pull hello-world) > paste inside docker dekstop terminal(now it will downloaded).

>run this command docker run -p 8501:8501 image_name > now run "localhost 8501" in google>your app will open.

![image](https://github.com/user-attachments/assets/549d8f2c-d968-4fe2-a4d5-8795b7a08650)



In a nut shell we learnt how to pull image from Docker Hub and run an application using docker dekstop.


# Dockerising Application & Pushing to Docker Hub
(Sample project is fastapi docker image is create see files)

## A.Dockerising Application
Step 1.Build an application inside any directory(Make sure its not inside the OneDrive folder because it restricts docker to build docker image due to permission,etc issue) 

Step 2:Prepare correct Dockerfile

Step 3:Build Docker image (from folder where your Dockerfile is):

![image](https://github.com/user-attachments/assets/ab697ad2-07d6-4c31-91e9-af425d50d4eb)

Step 4:![image](https://github.com/user-attachments/assets/9275a1ea-df8f-4f0a-aaec-be5e1d40f856)
![image](https://github.com/user-attachments/assets/9275a1ea-df8f-4f0a-aaec-be5e1d40f856)


### On succeessful docker image creation,Installed dependencies correctly & Launched the container o/p will be like
![image](https://github.com/user-attachments/assets/fc2c2f08-23a0-4549-a4af-2941cae36283)
![image](https://github.com/user-attachments/assets/d36c1a9c-6f02-4ebd-85a6-f9616a6a02b1)


## If app is running inside the container:o/p will be
![image](https://github.com/user-attachments/assets/c956b94f-b5d1-46dd-8ef4-2cefb2523f11)

## PORT MAPPING
## 📌 1. Port Mapping Kya Hai?

**Saral shabdon mein:**  
Port mapping aapke computer (jise **Host** kehte hain) ke port ko Docker container ke andar chal rahi application ke port se jodne ka ek tareeka hai.

**Kyun zaroori hai?**  
Docker containers apne aap mein **isolated (alag-thalag)** environments hote hain.  
Bina port mapping ke, aap container ke andar chal rahi application ko apne computer ke browser se access nahi kar sakte.  
Port mapping ek **pul (bridge)** ki tarah kaam karta hai jo host aur container ko connect karta hai.

---

## 📌 2. Command Ka Format

```bash

docker run -p <Host_Port>:<Container_Port> <image_name>

```
# IMPORTANT OBSERVATIONS..

1. Dockerfile me koi bhi badlav ke baad — nayi image build karo + naya container run karo.
2. Its recommended to create new directory(eg:app),set it as WORKDIR,copy ALL local files & directory into it.
![image](https://github.com/user-attachments/assets/92926c45-858c-4d57-bd4f-89bd350c74c2)
3.write http://localhost/t/docs [where docker run -p t:8000 containername,t is hostport] to acccess backend.
4.For development dont make debv directory inside OneDrive.

