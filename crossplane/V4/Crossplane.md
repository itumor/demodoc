# Install the Crossplane command-line 
To build a configuration package install the Crossplane Kubernetes command-line 
extension.

```bash
curl "https://raw.githubusercontent.com/crossplane/crossplane/master/install.sh"
./install.sh
sudo mv kubectl-crossplane /usr/bin
```

# Build a configuration package 
Use the kubectl crossplane command to create an .xpkg file containing the custom APIs and Crossplane configuration.

```bash
kubectl crossplane build configuration -f crossplane-aws-quickstart/ --name="crossplane-aws-quickstart"
```
Now an .xpkg OCI image is inside the crossplane-aws-quickstart directory.

```
ls crossplane-aws-quickstart/

```
# docker login

```
docker login
```

# Push a configuration package

```
cd crossplane-aws-quickstart
kubectl crossplane  push configuration  huma/crossplane-aws-quickstart:v0.0.1 -f crossplane-aws-quickstart.xpkg
```

https://hub.docker.com/r/huma/crossplane-aws-quickstart/tags


# up - The Upbound CLI
## Install
Homebrew
```
brew install upbound/tap/up
```


# Upbound Login Upbound
```
up login
```

# Build Package Upbound
```
VERSION_TAG=v0.0.1
up xpkg build --name crossplane-aws-quickstart.xpkg
```
# push Package Upbound
```
up xpkg push xpkg.upbound.io/itumor2005/crossplane-aws-quickstart:${VERSION_TAG} -f crossplane-aws-quickstart.xpkg
```

https://marketplace.upbound.io/account/itumor2005