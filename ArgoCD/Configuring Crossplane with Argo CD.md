
```bash
kubectl edit configmap argocd-cm -nargocd
```

```yaml
apiVersion: v1
data:
  application.resourceTrackingMethod: annotation
kind: ConfigMap

```

https://docs.crossplane.io/knowledge-base/integrations/argo-cd-crossplane/

```bash
kubectl get configmap argocd-cm -nargocd -o yaml> argocd-cm.yaml
```
```bash
kubectl apply -f argocd-cm.yaml
```

