# argocd
```bash
kubectl create namespace argocd
```

```bash
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

```

#  Download Argo CD CLI Homebrew:
```
brew install argocd
```

# Service Type Load Balancer
```
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```

# argocd pods
kubectl get pods -n argocd

# Port Forwarding
```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

# Login Using The CLI
```
argocd admin initial-password -n argocd
argocd login 127.0.0.1:8080
```

# Change the password using the command:
```
argocd account update-password 
```
# login
https://127.0.0.1:8080/login
```
argocd login 127.0.0.1:8080
admin
cpJ!8WHd9l45
```

