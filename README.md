Java DevOps Project with Jenkins, Docker, Kubernetes and Terraform

I built this project to understand how a real DevOps workflow works from start to end. Instead of focusing only on writing a Java application, I wanted to see how everything connects together like build, pipeline, container, deployment and infrastructure.

What this project does

This project takes a simple Java application and runs it through a full flow.

The application is built using Maven  
Jenkins pipeline is used to compile, test and package the code  
Docker is used to run the application in a container  
Kubernetes configuration is included to deploy the application  
Terraform is used to create AWS infrastructure including VPC and EKS  

Technologies used

Java  
Maven  
Jenkins  
Docker  
Kubernetes  
Terraform  
AWS  

How the flow works

When code is pushed, Jenkins runs the pipeline. It compiles the code, runs tests and packages the application. After that, a Docker image can be built. Terraform can be used to create AWS infrastructure like EKS. Then the Kubernetes file can be used to deploy the application inside the cluster.

Project structure

src contains the Java source code  
pom.xml is the Maven configuration  
Jenkinsfile is the pipeline definition  
Dockerfile is used to build the container  
deployment-service.yml is the Kubernetes configuration  
EKS_Terraform contains Terraform files for AWS infrastructure  
mvnw and mvnw.cmd are Maven wrapper files  
README.md is the project documentation  

How to run locally

First build the application using Maven  
mvn clean package  

Then build the Docker image  
docker build -t java-app .  

Run the container  
docker run -p 8080:8080 java-app  

Terraform setup

Terraform is used to create infrastructure in AWS. It creates VPC, subnets, internet gateway, security groups, EKS cluster and node group.

To run Terraform  
cd EKS_Terraform  
terraform init  
terraform apply  

Kubernetes

The deployment and service configuration is included. It can be used to deploy the application inside the EKS cluster.
