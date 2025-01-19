# Introduction 
TODO: Give a short introduction of your project. Let this section explain the objectives or the motivation behind this project. 

# Getting Started
TODO: Guide users through getting your code up and running on their own system. In this section you can talk about:
1.	Using the strategy

```bash
kubectl apply -f service.yml
kubectl apply -f nginx-blue-configmap.yml
kubectl apply -f nginx-green-configmap.yml
kubectl apply -f nginx-blue-deployment.yml
kubectl apply -f nginx-green-deployment.yml
```

2.	Check the strategy whether it works correctly

```bash
kubectl port-forward service/nginx-service 4200:80
```

```bash
curl localhost:8080
```

3.	Swap between them
Change the value of version that we want to pick in service yaml at node.

Either
```yaml
spec:
  selector:
    version: green
```
or
```yaml
spec:
  selector:
    version: green
```

4.	Remove the strategy
```bash
kubectl delete -f service.yml
kubectl delete -f nginx-blue-configmap.yml
kubectl delete -f nginx-green-configmap.yml
kubectl delete -f nginx-blue-deployment.yml
kubectl delete -f nginx-green-deployment.yml
```
