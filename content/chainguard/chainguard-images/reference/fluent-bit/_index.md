---
title: "Image Overview: fluent-bit"
linktitle: "fluent-bit"
type: "article"
layout: "single"
description: "Overview: fluent-bit Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/fluent-bit/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/fluent-bit/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/fluent-bit/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/fluent-bit/provenance_info/" >}}
{{</ tabs >}}



<!--overview:start-->
[Fluent Bit](https://fluentbit.io) is a lightweight and high performance log processor.
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/fluent-bit:latest
```
<!--getting:end-->

<!--body:start-->
## Using fluent-bit

Run a Fluent Bit instance that will receive messages over TCP port 24224 through the Forward protocol, and send the messages to the STDOUT interface in JSON format every second:

```sh
docker run -p 127.0.0.1:24224:24224 cgr.dev/chainguard/fluent-bit /usr/bin/fluent-bit -i forward -o stdout -p format=json_lines -f 1
```

Now run a separate container that will send a test message. This time the Docker container will use the Fluent Forward Protocol as the logging driver:

```sh
docker run --log-driver=fluentd -t ubuntu echo "Testing a log message"
```

On Fluent Bit container, it will print to stdout something like this:

```sh
Fluent Bit v2.0.8
* Copyright (C) 2015-2022 The Fluent Bit Authors
* Fluent Bit is a CNCF sub-project under the umbrella of Fluentd
* https://fluentbit.io

[2023/01/20 01:37:06] [ info] [fluent bit] version=2.0.8, commit=, pid=1
[2023/01/20 01:37:06] [ info] [storage] ver=1.4.0, type=memory, sync=normal, checksum=off, max_chunks_up=128
[2023/01/20 01:37:06] [ info] [cmetrics] version=0.5.8
[2023/01/20 01:37:06] [ info] [ctraces ] version=0.2.7
[2023/01/20 01:37:06] [ info] [input:forward:forward.0] initializing
[2023/01/20 01:37:06] [ info] [input:forward:forward.0] storage_strategy='memory' (memory only)
[2023/01/20 01:37:06] [ info] [input:forward:forward.0] listening on 0.0.0.0:24224
[2023/01/20 01:37:06] [ info] [sp] stream processor started
[2023/01/20 01:37:06] [ info] [output:stdout:stdout.0] worker #0 started
{"date":1674178633.0,"container_id":"c77d18c7700cc8e552b1f137ec9e6cd922637c733463e38fc97de7d51a95e4e9","container_name":"/nice_morse","source":"stdout","log":"Testing a log message\r"}
```
## Using the fluent-bit Helm Chart

You can deploy fluent-bit as a Helm chart by running the following:

```shell
helm repo add fluent https://fluent.github.io/helm-charts
helm repo update
```

Next, we can install it with the following command:

```shell
helm upgrade --install fluent-bit \
    --set image.repository=cgr.dev/chainguard/fluent-bit \
    --set image.tag=latest \
    --set command="/usr/bin/fluent-bit" \
    fluent/fluent-bit
```
<!--body:end-->

