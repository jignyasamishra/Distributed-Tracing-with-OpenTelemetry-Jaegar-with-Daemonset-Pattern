# Distributed Tracing with OpenTelemetry for Microservices
This project is a simple Microservices application providing a REST API to hit at its endpoints. The application communicates wuith each other and returns hello and spome random facts in JSON and includes OpenTelemetry tracing to send trace data to a distributed tracing backend via an OpenTelemetry Collector.
# Architecture
## Full scale architecture
![image](https://github.com/user-attachments/assets/54312c35-9b7b-4b2d-80b6-984a04f177e2)
# Pre-requisites 
- Working K8s cluster
- Cert-manager deployed for certificates generation by Jaeagr operator
# Install Jaegar Operator
```
kubectl create ns observability
kubectl apply -f jaegar-operator.yaml
```
# Install OpenTel Operator
```
kubectl apply -f opentel-operator.yaml
```
# Install Jaeagr Custom Resource
``` 
kubectl apply -f jaegar.yaml
```
# Install OpenTel colllector Daemonset
```
kubectl apply -f opentel-collector-ds.yaml
```
# Install OpenTel colllector Deployment
```
kubectl apply -f opentel-collector.yaml
```
# Test it locally 

```
 kubectl apply -f demonset-pattern/app.yaml

```
