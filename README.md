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
# Results
![image](https://github.com/user-attachments/assets/0ae787bc-0389-4fbc-8f45-70062eb74c75)
![image](https://github.com/user-attachments/assets/8a108a00-bc1b-4ded-be90-e0a575e2a3e4)
![image](https://github.com/user-attachments/assets/7cd90262-a89e-4e5a-9c87-c07e94460cb2)




