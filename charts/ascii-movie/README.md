# ascii-movie

<img src="https://raw.githubusercontent.com/gabe565/ascii-movie/a1fd5c9df2fb3a177949c9511b62407c83aedefe/assets/icon.svg" align="right" width="92" alt="ascii-movie logo">

![Version: 0.6.2](https://img.shields.io/badge/Version-0.6.2-informational?style=flat)
![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat)
![AppVersion: 1.2.2](https://img.shields.io/badge/AppVersion-1.2.2-informational?style=flat)

Star Wars movie SSH and Telnet server

**Homepage:** <https://charts.gabe565.com/charts/ascii-movie>

**This chart is not maintained by the upstream project and any issues with the chart should be raised
[here](https://github.com/gabe565/charts/issues/new?assignees=gabe565&labels=bug&template=bug_report.yaml&name=ascii-movie&version=0.6.2)**

## Source Code

* <https://github.com/gabe565/ascii-movie>

## Requirements

Kubernetes: `>=1.22.0-0`

## Dependencies

| Repository | Name | Version |
|------------|------|---------|
| <https://bjw-s.github.io/helm-charts> | common | 1.3.2 |

## TL;DR

```console
helm repo add gabe565 https://charts.gabe565.com
helm repo update
helm install ascii-movie gabe565/ascii-movie
```

## Installing the Chart

To install the chart with the release name `ascii-movie`

```console
helm install ascii-movie gabe565/ascii-movie
```

## Uninstalling the Chart

To uninstall the `ascii-movie` deployment

```console
helm uninstall ascii-movie
```

The command removes all the Kubernetes components associated with the chart **including persistent volumes** and deletes the release.

## Configuration

Read through the [values.yaml](./values.yaml) file. It has several commented out suggested values.
Other values may be used from the [values.yaml](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common/values.yaml) from the [bjw-s common library](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common).

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`.

```console
helm install ascii-movie \
  --set env.TZ="America/New York" \
    gabe565/ascii-movie
```

Alternatively, a YAML file that specifies the values for the above parameters can be provided while installing the chart.

```console
helm install ascii-movie gabe565/ascii-movie -f values.yaml
```

## Custom configuration

N/A

## Values

**Important**: When deploying an application Helm chart you can add more values from the bjw-s common library chart [here](https://github.com/bjw-s/helm-charts/tree/main/charts/library/common)

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| controller.strategy | string | `"RollingUpdate"` | Set the controller upgrade strategy |
| image.pullPolicy | string | `"Always"` | image pull policy |
| image.repository | string | `"ghcr.io/gabe565/ascii-movie"` | image repository. |
| image.tag | string | `"1.2.2"` | image tag |
| service | object | See [values.yaml](./values.yaml) | Configures service settings for the chart. |

---
Autogenerated from chart metadata using [helm-docs](https://github.com/norwoodj/helm-docs)