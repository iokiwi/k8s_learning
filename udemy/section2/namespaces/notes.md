switch namespace for current context

```bash
kubectl config set-context $(kubectl config current-context) --namespace=dev
```
