# Introduction to Kubernetes

To run this Kubernetes-based project locally, you will need to have Kubernetes and Minikube installed on your machine. The project consists of a MongoDB database and a web application that connects to it. Here's a step-by-step guide to get the project up and running:

## Prerequisites
- Install Docker
- Install Minikube
- Install kubectl

### Steps to Run the Project
Start Minikube
Start your Minikube cluster to create a local Kubernetes cluster:

```sh
minikube start
```

### Apply MongoDB Configurations
Apply the MongoDB configuration and secret files to set up the MongoDB environment:

```sh
kubectl apply -f mongo-config.yaml
kubectl apply -f secret.yaml
```

### Deploy MongoDB
Deploy the MongoDB application:

```sh
kubectl apply -f mongo-app.yaml
```

### Deploy Web Application
Deploy the web application that connects to MongoDB:

```sh
kubectl apply -f web-app.yaml
```
### Check All Pods
To verify that all pods are up and running, use the following command:

```sh
kubectl get pods
```
### Accessing the Web Application
To access the web application through Minikube, use the minikube service command which automatically opens the service in your default browser:

```sh
minikube service web-service
```
