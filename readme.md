## Helm Chart Repositories for Kubernetes

### List of available Charts in this repo:
- ### [Frontend and Backend Chart together in consul]()
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
Generate index.yaml:
```shell
helm repo index .
```


make package to .tgz zip
```shell
helm package $(pwd)/ -d $(pwd)/
```

```shell
helm package .
```

Successfully packaged chart and saved it to: ../app-0.1.0.tgz