# Helm Chart: Frontend and Backend Deployment with Consul Service Mesh

This Helm Chart enables the deployment of both Frontend and Backend services separately while utilizing the capabilities of the Consul service mesh.

-------------------------------------
## Usage
The chart can be utilized either manually or in conjunction with Terragrunt.

### Add Helm Repository
```bash
helm repo add my-repo-name https://DTG-cisco/github.io/helm-charts/
```

### Install the Chart
```shell
helm install my-release-name my-repo-name/chart-name
helm install my-release-name charts/fe_be_chart
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