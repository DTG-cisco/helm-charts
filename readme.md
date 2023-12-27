## Helm Chart Repositories for Kubernetes

### List of available Charts in this repo:
- ### [Frontend Chart for consul](charts/frontend/Readme.md)
- ### [Backend Chart for consul](charts/backend/Readme.md)
- ### [Consul API Gateway](charts/api-gateway/readme.md)

-----------------------------------
## How to use
You can follow [Helm Docs](https://helm.sh/docs/intro/quickstart/) 

### Add Helm Repository
```shell
helm repo add schedule-app  https://dtg-cisco.github.io/helm-charts/
```

#### Get list of available versions:
```shell
helm search repo schedule-app
```
In list of available versions select needed:

| NAME                  | CHART VERSION | APP VERSION | DESCRIPTION                                        | 
|-----------------------|---------------|-------------|----------------------------------------------------|
| schedule-app/frontend | 0.0.2         | 0.1.2       | Frontback And Backend (Local PSQL DB) are succe... |
| schedule-app/backend  | 0.0.1         | 0.1.2       | A Helm chart for Kubernetes, Frontback And Back... |


### Install the Chart
```text
helm install <my-release-name> <my-repo-name>/<chart-name>
```
```shell
helm install front schedule-app/frontend
```

### Configuration
```bash
helm install <my-release-name> <my-repo-name>/<chart-name> --set key1=value1,key2=value2
```

### Upgrade or Uninstall
```shell
# Upgrade
helm upgrade my-release-name my-repo-name/chart-name
```
```bash
# Uninstall
helm uninstall front
```