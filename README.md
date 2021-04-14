Create cluster

https://docs.catalystcloud.nz/kubernetes/quickstart.html

```bash
openstack coe cluster create \
  --cluster-template kubernetes-v1.19.6-dev-20210211 \
  --keypair simon-key \
  --master-flavor c1.c2r8 \
  --flavor c1.c2r8 \
  simon-ckad
```

```bash
stack_id=$(openstack stack list | grep simon-ckad | awk '{ print $2 }')
watch -n 2 -d openstack stack resource list $stack_id
```

```bash
eval $(openstack coe cluster config simon-ckad)
```