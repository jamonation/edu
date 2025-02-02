---
title: "prometheus-alertmanager Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public prometheus-alertmanager Chainguard Image variants"
date: 2023-03-07T11:07:52+02:00
lastmod: 2024-02-14 00:20:21
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/prometheus-alertmanager/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/prometheus-alertmanager/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/prometheus-alertmanager/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/prometheus-alertmanager/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **prometheus-alertmanager** Image.

## Variants Compared
The **prometheus-alertmanager** Chainguard Image currently has 2 public variants: 

- `latest-dev`
- `latest`

The table has detailed information about each of these variants.

|              | latest-dev                                                                      | latest                                                                          |
|--------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Default User | `alertmanager`                                                                  | `alertmanager`                                                                  |
| Entrypoint   | `/usr/bin/alertmanager`                                                         | `/usr/bin/alertmanager`                                                         |
| CMD          | `--config.file=/etc/alertmanager/alertmanager.yml --storage.path=/alertmanager` | `--config.file=/etc/alertmanager/alertmanager.yml --storage.path=/alertmanager` |
| Workdir      | not specified                                                                   | not specified                                                                   |
| Has apk?     | yes                                                                             | yes                                                                             |
| Has a shell? | yes                                                                             | yes                                                                             |

Check the [tags history page](/chainguard/chainguard-images/reference/prometheus-alertmanager/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                           | latest-dev | latest |
|---------------------------|------------|--------|
| `apk-tools`               | X          | X      |
| `bash`                    | X          |        |
| `busybox`                 | X          | X      |
| `ca-certificates-bundle`  | X          | X      |
| `git`                     | X          |        |
| `glibc`                   | X          | X      |
| `glibc-locale-posix`      | X          | X      |
| `ld-linux`                | X          | X      |
| `libbrotlicommon1`        | X          |        |
| `libbrotlidec1`           | X          |        |
| `libcrypt1`               | X          | X      |
| `libcrypto3`              | X          | X      |
| `libcurl-openssl4`        | X          |        |
| `libexpat1`               | X          |        |
| `libidn2`                 | X          |        |
| `libnghttp2-14`           | X          |        |
| `libpcre2-8-0`            | X          |        |
| `libpsl`                  | X          |        |
| `libssl3`                 | X          | X      |
| `libunistring`            | X          |        |
| `ncurses`                 | X          |        |
| `ncurses-terminfo-base`   | X          |        |
| `openssl-config`          | X          | X      |
| `prometheus-alertmanager` | X          | X      |
| `wget`                    | X          |        |
| `wolfi-base`              | X          | X      |
| `wolfi-baselayout`        | X          | X      |
| `wolfi-keys`              | X          | X      |
| `zlib`                    | X          | X      |

