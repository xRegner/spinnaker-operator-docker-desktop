# login k8s

```bash
#only if azure
az aks get-credentials --resource-group <rg>  --name <cluster-name> 
```

```bash
  kubectl apply -f deploy/crds/
  kubectl create ns spinnaker-operator
  kubectl -n spinnaker-operator apply -f deploy/operator/cluster
  kubectl -n spinnaker-operator apply -f deploy/spinnaker/basic/spinnakerservice-az.yml

```

## only if local


```bash
kubectl apply -f deploy/crds/
kubectl create ns spinnaker-operator
kubectl -n spinnaker-operator apply -f deploy/operator/cluster
kubectl -n spinnaker-operator apply -f deploy/spinnaker/docker-local/.

```

## to delete

```bash
kubectl delete -f deploy/crds/

kubectl -n spinnaker-operator delete -f deploy/operator/cluster
kubectl -n spinnaker-operator delete -f deploy/spinnaker/docker-local/.
kubectl delete ns spinnaker-operator
```
