# istio-operator

![Version: 1.13.2-bb.1](https://img.shields.io/badge/Version-1.13.2--bb.1-informational?style=flat-square) ![AppVersion: 1.13.2](https://img.shields.io/badge/AppVersion-1.13.2-informational?style=flat-square)

Helm chart for deploying Istio operator

## Upstream References

* <https://github.com/istio/istio/tree/master/operator>

## Learn More
* [Application Overview](docs/overview.md)
* [Other Documentation](docs/)

## Pre-Requisites

* Kubernetes Cluster deployed
* Kubernetes config installed in `~/.kube/config`
* Helm installed

Install Helm

https://helm.sh/docs/intro/install/

## Deployment

* Clone down the repository
* cd into directory
```bash
helm install istio-operator chart/
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| hub | string | `"registry1.dso.mil/ironbank/opensource/istio"` |  |
| image | string | `"operator"` |  |
| tag | string | `"1.13.2"` |  |
| enterprise | bool | `false` | Tetrate Istio Distribution - Tetrate provides FIPs verified Istio and Envoy software and support, validated through the FIPs Boring Crypto module. Find out more from Tetrate - https://www.tetrate.io/tetrate-istio-subscription |
| tidHub | string | `"registry1.dso.mil/ironbank/tetrate/istio"` |  |
| tidTag | string | `"1.12.4-tetratefips-v0"` |  |
| imagePullPolicy | string | `"IfNotPresent"` |  |
| imagePullSecrets | list | `[]` |  |
| watchedNamespaces | string | `"istio-system"` |  |
| waitForResourcesTimeout | string | `"300s"` |  |
| enableCRDTemplates | bool | `false` |  |
| revision | string | `""` |  |
| operator.resources.limits.cpu | string | `"200m"` |  |
| operator.resources.limits.memory | string | `"256Mi"` |  |
| operator.resources.requests.cpu | string | `"200m"` |  |
| operator.resources.requests.memory | string | `"256Mi"` |  |
| createNamespace | bool | `true` |  |
| nodeSelector | object | `{}` |  |
| affinity | object | `{}` |  |
| monitoring.enabled | bool | `false` |  |
| networkPolicies.enabled | bool | `false` |  |
| networkPolicies.controlPlaneCidr | string | `"0.0.0.0/0"` |  |

## Contributing

Please see the [contributing guide](./CONTRIBUTING.md) if you are interested in contributing.
