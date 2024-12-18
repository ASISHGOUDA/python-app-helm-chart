# Python Flask REST API Helm Chart Deployment

This repository contains a Helm chart to deploy a Python Flask-based REST API application on Kubernetes. The chart is designed to be easy to use and configure for your environment.

## Prerequisites

Before you begin, ensure that you have the following installed:

- Kubernetes cluster (minikube, AWS EKS, GKE, etc.)
- Helm 3.x
- kubectl

## Installation

To install and deploy the `python-app-helm-chart` using Helm, follow these steps:

### 1. Clone the repository

Clone this repository to your local machine if you haven't already.

```bash
git clone https://github.com/your-repo/python-app-helm-chart.git
cd python-app-helm-chart
```

### 2. Add Kubernetes Cluster Context

Ensure that your kubectl is configured to use the correct Kubernetes context.

```bash
kubectl config use-context <your-context>
```

### 3. Install the Helm Chart

Use the following Helm command to install the Python Flask REST API:

```bash
helm install python-app-release python-app-helm-chart
```

This will deploy the application using the Helm chart in the current directory. By default, it will create the necessary Kubernetes resources (like Deployments, Services, and ConfigMaps).

### 4. Access the Application

After deploying the application, you can access it via the following IP address and port:

```
http://172.29.221.135:32077
```

To confirm that the application is running, you can check the status of the deployed resources:

```bash
kubectl get all
```

This will show the Pods, Services, and other resources created by the Helm chart.

### 5. Uninstall the Application

To uninstall the Python Flask REST API application and remove all associated resources, use the following Helm command:

```bash
helm uninstall python-app-release
```
This will delete the release and clean up all the Kubernetes resources.