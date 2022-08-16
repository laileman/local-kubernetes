# reference
- https://openebs.github.io/charts/
- https://openebs.io/

# deploy
```
helm repo add openebs https://openebs.github.io/charts
helm repo update
helm install openebs --namespace openebs openebs/openebs --create-namespace
```
# upgrade
```
helm upgrade openebs openebs/openebs \
        --namespace openebs \
        --set legacy.enabled=true \
        --reuse-values

helm upgrade openebs openebs/openebs \
        --namespace openebs \
        --set cstor.enabled=true \
        --reuse-values
```

# advance deply
```

```

