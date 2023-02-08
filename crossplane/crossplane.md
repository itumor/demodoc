```
helm repo add \
crossplane-stable https://charts.crossplane.io/stable
helm repo update
```
```
helm install crossplane \
crossplane-stable/crossplane \
--namespace crossplane-system \
--create-namespace
```

```
kubectl get all  -n  crossplane-system
```

```
kubectl get crds | grep crossplane 
```