This project deploys two services on Kubernetes:

- Payment Gateway
- Payment Processor

The Gateway communicates with the Processor using the Kubernetes Service name.

## Architecture

Client
   |
   v
Payment Gateway
   |
   v
Payment Processor

## Prerequisites

- Docker
- Kubernetes
- kubectl

## Deploy

Apply the processor:

kubectl apply -f processor-deployment.yaml
kubectl apply -f processor-service.yaml

Apply the gateway:

kubectl apply -f gateway-deployment.yaml
kubectl apply -f gateway-service.yaml

## Check Pods

kubectl get pods

## Check Services

kubectl get services

## Test

Access the gateway on:

http://localhost:30080

## Remove Deployment

kubectl delete -f gateway-deployment.yaml
kubectl delete -f gateway-service.yaml
kubectl delete -f processor-deployment.yaml
kubectl delete -f processor-service.yaml
