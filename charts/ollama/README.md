# Ollama Helm Chart

This directory contains a Helm chart to deploy an ollama instance with a gemma3 model included.

## Chart Details

This chart will do the following:

- Install a deployment running gemma3 with a service for its API. It does not include a route, as it is intended for internal use only.

## Usages

### Add this chart repository

```console
$ helm repo add sso-charts https://bcgov.github.io/sso-helm-charts
```

### Install this chart repository

```console
$ helm install <release-name> sso-charts/ollama [--namespace <my-namespace>] [--version <x.y.z>] [--values ./custom-values.yaml]
```

### Upgrade this chart repository

```console
$ helm upgrade <release-name> sso-charts/ollama [--namespace <my-namespace>] [--version <x.y.z>] [--values ./custom-values.yaml]
```

### Uninstall this chart repository

```console
$ helm uninstall <release-name> [--namespace <my-namespace>]
```
