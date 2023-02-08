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