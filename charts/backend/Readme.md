# Helm Chart: Backend Deployment with Consul Service Mesh

This Helm Chart enables the deployment of Backend service separately while utilizing the capabilities of the Consul service mesh.

-------------------------------------
## Usage
The chart can be utilized either manually or in conjunction with Terragrunt.

### Add Helm Repository
```bash
helm repo add schedule-app  https://dtg-cisco.github.io/helm-charts/
```
#### Get list of available versions:
```shell
helm search repo schedule-app 
```
| NAME                 | CHART VERSION | APP VERSION | DESCRIPTION              | 
|----------------------|---------------|-------------|--------------------------|
| schedule-app/backend | 0.0.1         | 0.1.2       | Backend chart for Consul |


### Install the Chart
```shell
helm install back schedule-app/backend 
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
helm uninstall back
```

------------------------------
### How to create new version

Make package from Chart to .tgz zip
```shell
helm package charts/backend/ -d  packages/
```
Output: Successfully packaged chart and saved it to: packages/backend-0.1.2.tgz


Generate index.yaml:
```shell
helm repo index .
```