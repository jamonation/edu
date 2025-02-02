---
title: "Image Overview: cass-config-builder"
linktitle: "cass-config-builder"
type: "article"
layout: "single"
description: "Overview: cass-config-builder Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/cass-config-builder/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/cass-config-builder/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/cass-config-builder/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/cass-config-builder/provenance_info/" >}}
{{</ tabs >}}



<!--overview:start-->
Minimal [cass-config-builder](https://github.com/datastax/cass-config-builder) container image.
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/cass-config-builder:latest
```
<!--getting:end-->

<!--body:start-->

To use this image you can follow up the official documentation of installing the Helm Chart for K8ssandra Operator, [here](https://docs.k8ssandra.io/install/).

In the [ImageConfiguration](https://docs.k8ssandra.io/install/image-config/) section which allows you to configure the K8ssandra images to use custom registries or custom images, you can use the the this image for the `cass-config-builder` image config, [here](https://github.com/k8ssandra/cass-operator/blob/ff5bc87f10b890ab09eb2d5c369edf2568169dd8/config/manager/image_config.yaml#L7) as an example:

```yaml
apiVersion: config.k8ssandra.io/v1beta1
kind: ImageConfig
metadata:
  name: image-config
images:
...
  config-builder: "cgr.dev/chainguard/cass-config-builder:latest"
...
```

If you do this change right after your installation, you might need to delete the pods under the `k8ssandra-operator` namespace for the changes to take effect by the pods being recreated but please verify that the pods are up and running before proceeding with the next steps.

Next, to test the image whether it is actually working you should create `K8ssandraCluster` CR with the following spec, [here](https://docs.k8ssandra.io/install/local/single-cluster-helm/#deploy-the-k8ssandracluster):

```yaml
apiVersion: k8ssandra.io/v1alpha1
kind: K8ssandraCluster
metadata:
  name: demo
  namespace: k8ssandra-operator
spec:
  cassandra:
    serverVersion: "4.0.1"
    datacenters:
      - metadata:
          name: dc1
        size: 3
        storageConfig:
          cassandraDataVolumeClaimSpec:
            storageClassName: standard # make sure that you configure this to match your environment
            accessModes:
              - ReadWriteOnce
            resources:
              requests:
                storage: 5Gi
        config:
          jvmOptions:
            heapSize: 512M
        stargate:
          size: 1
          heapSize: 256M
```

After you created the `K8ssandraCluster` CR, there should be a pod with the name `demo-dc1-default-sts-0` under the `k8ssandra-operator` namespace up and running because the `cass-config-builder` image is going to be used as an initContainer so if the pod is up and running we can confirm that the image is working as expected.
<!--body:end-->

