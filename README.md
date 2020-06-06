# kubernetes sample apps in python flask framework
This is a repository created to manage all kubernetes tutorials to deploy flask based sample applications.
We can deploy the application in kubernetes cluster using kubectl commands or using YAML configuration files.In this examples we are deploying it using YAML files.

## Prerequisites
Make sure you have installed all of the following prerequisites on your development machine:
* kubectl : Kubectl is a command line tool for controlling Kubernetes clusters[https://kubernetes.io/docs/reference/kubectl/overview/].
* Minikube :Minikube is a tool that makes it easy to run Kubernetes locally [https://kubernetes.io/docs/setup/learning-environment/minikube/]. After install start also minikube by the command : minikube start

## Application 1 : httpd-app

Here we have created a two yaml files to deploy httpd for deployment and service respectively.
* Deployment file : httpd-basic-deployment.yml
    -   It will run a single container within a pod using a docker image "httpd" and it will listen on port 80
* Service file : httpd-basic-service.yml
    -   This file is for service that expose the port externally so that users will be able to access it.

Commands : 
```bash
cd httpd-app
kubectl apply -f httpd-basic-deployment.yml
kubectl apply -f httpd-basic-service.yml
```
Get the port number for the app by the command : 
Fetch the minikube ip by the command(minikube ip) 
Visit the URL : minikubeIp:portnumber
