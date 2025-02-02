---
title: "Image Overview: argo-workflowcontroller"
linktitle: "argo-workflowcontroller"
type: "article"
layout: "single"
description: "Overview: argo-workflowcontroller Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/argo-workflowcontroller/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/argo-workflowcontroller/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/argo-workflowcontroller/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/argo-workflowcontroller/provenance_info/" >}}
{{</ tabs >}}



<!--overview:start-->
Images for working with [Argo workflows](https://argoproj.github.io/argo-workflows/)
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/argo:latest
```
<!--getting:end-->

<!--body:start-->
## Versions

```
docker pull cgr.dev/chainguard/argo-exec
docker pull cgr.dev/chainguard/argo-cli
docker pull cgr.dev/chainguard/argo-workflowcontroller
```

## Using argo

Argo provides two upstream methods for installing, helm, and raw manifests.

The Chainguard Images for Argo are designed to be a drop in replacement for either method. To use them, simply replace the appropriate `image:` path with the Chainguard specific Argo image. Below is an example values file for doing this with helm:

```yaml

images:
  tag: "latest"
controller:
  image:
    # -- Registry to use for the controller
    registry: cgr.dev
    # -- Registry to use for the controller
    repository: chainguard/argo-workflow-controller
executor:
  image:
    # -- Registry to use for the Workflow Executors
    registry: cgr.dev
    # -- Repository to use for the Workflow Executors
    repository: chainguard/argo-exec
server:
  # -- Deploy the Argo Server
  image:
    # -- Registry to use for the server
    registry: cgr.dev
    # -- Repository to use for the server
    repository: chainguard/argo-cli
```

Using the above values, the helm commands become:

```bash
helm repo add argo https://argoproj.github.io/argo-helm

helm install argo-workflows argo/argo-workflows \
	--namespace argo-workflows \
	--create-namespace \
	--set images.tag="latest" \
	--set global.image.tag="latest" \
  --set controller.image.registry="cgr.dev" \
  --set controller.image.repository="chainguard/argo-workflow-controller" \
  --set executor.image.registry="cgr.dev" \
  --set executor.image.repository="chainguard/argo-exec" \
  --set server.image.registry="cgr.dev" \
  --set server.image.repository="chainguard/argo-cli"
```


> NOTE: Setting the tag to "latest" is not recommended, and only shown for illustrative purposes.
<!--body:end-->

