
What helped me:
- https://docs.microsoft.com/de-de/azure/container-service/kubernetes/container-service-kubernetes-walkthrough
- https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes-general

```
az group create --name bsb --location westeurope

az acs create --orchestrator-type kubernetes --resource-group bsb --name camundaCluster --generate-ssh-keys --agent-vm-size Standard_DS1 --agent-count 1

az acs kubernetes get-credentials --resource-group=bsb--name=camunda
```

Now you can use `kubectl`

```
kubectl apply -f ns.yaml
```


Helpful:
- https://gist.github.com/devigned/22bc246371d4eab24d01fb3c5d2fbc6a