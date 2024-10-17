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
kubectl create service clusterip my-service --tcp=80:80 --dry-run=client -o yaml > templates/service.yaml

```

# Chart Install

```
helm install first-release .
```