https://argo-cd.readthedocs.io/en/stable/operator-manual/cluster-bootstrapping/

# create apps
argocd app create apps \
    --dest-namespace argocd \
    --dest-server https://kubernetes.default.svc \
    --repo https://github.com/itumor/demodoc.git \
    --path apps  
argocd app sync apps  


# sync apps
argocd app sync -l app.kubernetes.io/instance=apps
# delete apps
argocd app delete apps 