This is a collection of [exec plugins][] for [kustomize][].

[kustomize]: https://github.com/kubernetes-sigs/kustomize
[exec plugins]: https://kubernetes-sigs.github.io/kustomize/guides/plugins/

## SOPS plugin

```
apiVersion: oddbit.com/v1
kind: Sops
metadata:
  name: secret-generator
files:
  - ./mysecret.yml
```

## GPG plugin

```
apiVersion: oddbit.com/v1
kind: Gpg
metadata:
  name: secret-generator
requireValidSignature: true
files:
  - ./mysecret.gpg
```

## Installation

### For use in all your projects

- Copy the `oddbit` directory from this repository into
  `~/.config/kustomize/plugin/`.

### For use in a single project

- Create a `kustomize/plugin` directory relative to your
  `kustomization.yml` file
- Copy the `oddbit` directory from this repository into `kustomize/plugin/`.
