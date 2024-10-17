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


# Helm Wordpress Install

* Visit (Official Documentation)[https://artifacthub.io/packages/helm/bitnami/wordpress?modal=install]
* `helm repo add bitnami https://charts.bitnami.com/bitnami`
* `helm install my-wordpress bitnami/wordpress --version 23.1.22`

**Add Manually**

* `helm pull --untar bitnami/wordpress --version 23.1.22`
* Upgrade wordpress with custom values: `helm upgrade my-wordpress . --values custom-values.yaml`
* Helm history check : `helm history my-wordpress`
* Helm rollbacke : `helm rollback my-wordpress 1`
