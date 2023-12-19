## Helm Chart Repositories for Kubernetes

### List of available Charts in this repo:
- ### [Frontend and Backend Chart together in consul](charts/fe_be_chart/Readme.md)
- ### [Frontend Chart]()
- ### [Backend Chart]()

### How to use
```shell
helm repo add schedule-app  https://vitalikys.github.io/chart/
```

Get list of available versions:
```shell
helm search repo schedule-app
```

### How to create new version
Create new Helm Chart revision in 


Make package from Chart to .tgz zip
```shell
helm package charts/fe_be_chart/ -d  packages/
```
Successfully packaged chart and saved it to: packages/fe_be_chart-0.0.1.tgz


Generate index.yaml:
```shell
helm repo index .
```