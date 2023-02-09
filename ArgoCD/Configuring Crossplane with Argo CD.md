
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


kubectl describe configmaps argocd-cm -n argocd
kubectl edit configmaps argocd-cm -n argocd

```yaml
data:
  timeout.reconciliation: 60s
  application.resourceTrackingMethod: annotation
```

```
kubectl -n argocd rollout restart deploy argocd-repo-server
```
