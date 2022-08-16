# Prerequisites

* Kubernetes: `>= 1.16.0-0`
* Helm: `>= 3.0`

# Reference
deply by helm: https://docs.cilium.io/en/stable/gettingstarted/k8s-install-helm/


# deploy
- cilium
```bash
helm repo add cilium https://helm.cilium.io/
helm install cilium cilium/cilium --version 1.12.0 \
  --namespace cni --create-namespace --dry-run

```

- hubble
```bash
helm upgrade cilium cilium/cilium --version 1.12.0 \
   --namespace cni \
   --reuse-values \
   --set hubble.relay.enabled=true \
   --set hubble.ui.enabled=true
```

# advance deploy
```
helm install cilium cilium/cilium --version 1.12.0 \
  --namespace cni --create-namespace -f  values.yaml --dry-run
```

# helm update
```
helm upgrade -n cni cilium cilium/cilium -f values.yaml  
```