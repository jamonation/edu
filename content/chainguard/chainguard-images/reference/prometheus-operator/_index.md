---
title: "Image Overview: prometheus-operator"
linktitle: "prometheus-operator"
type: "article"
layout: "single"
description: "Overview: prometheus-operator Chainguard Image"
date: 2022-11-01T11:07:52+02:00
lastmod: 2024-02-16 00:30:51
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
menu: 
  docs: 
    parent: "images-reference"
weight: 500
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/prometheus-operator/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/prometheus-operator/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/prometheus-operator/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/prometheus-operator/provenance_info/" >}}
{{</ tabs >}}



<!--overview:start-->
Minimalist Wolfi-based image for Prometheus Operator. Prometheus Operator creates/configures/manages Prometheus clusters atop Kubernetes
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/prometheus-operator:latest
```
<!--getting:end-->

<!--body:start-->

## Usage
For full instructions on prometheus-operator, refer to the
[official documentation](https://prometheus-operator.dev).
The GitHub repository can also be [found here](https://github.com/prometheus-operator/prometheus-operator).

### Helm
To deploy via helm, please refer to the upstream
[helm charts documentation](https://github.com/prometheus-community/helm-charts)
for comprehensive instructions, which includes
[supported parameters](https://github.com/prometheus-community/helm-charts/blob/eef28b4b566c463242774814cfa5a94a9dec3e99/charts/kube-prometheus-stack/values.yaml#L2059)

Below is an example of how to use the helm chart, overriding the image with the
chainguard image:

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update

helm install prom-operator prometheus-community/kube-prometheus-stack \
 --set prometheusOperator.image.registry=cgr.dev \
 --set prometheusOperator.image.repository=chainguard/prometheus-operator \
 --set prometheusOperator.image.tag=latest
```
<!--body:end-->

