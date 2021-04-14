Edit in place
```
kubectl edit replicaset new-replica-set
```

```bash
kubectl get replicaset <name> -o yaml > <name>.yml
```

Scale replica set

```bash
kubectl replace -f replicaset-definition.yml
kubectl scale --replicas=6 -f replicaset-definition.yml
kubectl scale --replicas=6 replicaset myapp-replicaset
```
