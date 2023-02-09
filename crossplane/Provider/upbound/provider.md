kubectl-crossplane install provider xpkg.upbound.io/upbound/provider-aws:v0.27.0 upbound-provider-aws --config="debug-config" --verbose

kubectl get provider -w