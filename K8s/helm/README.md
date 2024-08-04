Use this helm chart to customise your install of Stan's Robot Shop.

### Helm v2.x

```shell
helm install --name robot-shop --namespace robot-shop .
```

### Helm v3.x

```bash
kubectl create ns robot-shop
helm install robot-shop --namespace robot-shop .
```

### Ingress Service

We are using ingress service to expose our application to external world.
```bash
kubectl apply -f ingress.yaml
```

Once your application is deployed successfully you can delete the cluster.
## Delete the cluster

```
eksctl delete cluster --name demo-cluster-three-tier-1 --region us-east-1
```