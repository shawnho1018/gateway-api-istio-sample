# gateway-api-istio-sample
This example demonstrates how to utilize kustomize to produce:
1. One Namespace, One Gateway:
Run the following command to deploy k8s service, gateway, and httproute to "single" namespace.  
```
kustomize build single/ | kubectl apply -f -
``` 
Once the deployment is completed, using the following command to check on ip address.
```
kubectl get gtw -n single
```

2. Dual Namespaces, One Gateway:
Run the following command to deploy 1 gateway, 2 httproutes, and 2 kubernetes services/deployments in separate namespaces, one & two. 
```
kustomize build dual/ | kubectl apply -f -
```
Once the deployment is completed, get the ip address with the following command:
```
kubectl get gtw -n one
```
