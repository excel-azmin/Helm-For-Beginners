# Create a Helm Chart

```
helm create my-first-chart
```

# Create Deployment File

```
kubectl create deploy my-deployment --image=nginx --dry-run=client -o yaml > templates/deploymnet.yaml
```

# Create Service File

```
kubectl create service clusterip/nodeport my-service --tcp=80:80 --dry-run=client -o yaml > templates/service.yaml

```

# Chart Install

```
helm install first-release .
```

# Basic Helm Command 

* Check helm syntex error : `helm lint .`
* Helm template : `helm template .`
* Helm list: `helm list`
* Uninstall helm : `helm uninstall app-name`
* Helm dry-run : `helm install my-chart . --dry-run`
* Helm help : `helm --help`