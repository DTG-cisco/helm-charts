# Helm Chart: Frontend and Backend Deployment with Consul Service Mesh

This Helm Chart enables the deployment of both Frontend and Backend services separately while utilizing the capabilities of the Consul service mesh.

-------------------------------------
## Usage
The chart can be utilized either manually or in conjunction with Terragrunt.

### Add Helm Repository
```bash
helm repo add my-consul  https://dtg-cisco.github.io/helm-charts/
```
#### Get list of available versions:
```shell
helm search repo my-consul
```
| NAME                   | CHART VERSION |  APP VERSION |  DESCRIPTION    | 
|------------------------|---------------|--------------|-----------------|
| my-consul/fe_be_chart  |   0.0.1       |    0.1.2     |  A Helm chart for Kubernetes, Frontback And Back...|


### Install the Chart
```shell
helm install my-release-name my-repo-name/chart-name
helm install my-release-name charts/app_chart
```

### Configuration
```bash
helm install my-release-name my-repo-name/chart-name --set key1=value1,key2=value2
```

### Upgrade or Uninstall
```shell
# Upgrade
helm upgrade my-release-name my-repo-name/chart-name

# Uninstall
helm uninstall my-release-name
```

------------------------------
### How to create new version

Make package from Chart to .tgz zip
```shell
helm package charts/app_chart/ -d  packages/
```
Successfully packaged chart and saved it to: packages/fe_be_chart-0.0.1.tgz


Generate index.yaml:
```shell
helm repo index .
```