---
title: "dask-gateway Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public dask-gateway Chainguard Image variants"
date: 2023-03-07T11:07:52+02:00
lastmod: 2024-02-08 00:18:32
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/dask-gateway/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/dask-gateway/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/dask-gateway/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/dask-gateway/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **dask-gateway** Image.

## Variants Compared
The **dask-gateway** Chainguard Image currently has 2 public variants: 

- `latest-dev`
- `latest`

The table has detailed information about each of these variants.

|              | latest-dev                                                                       | latest                                                                           |
|--------------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Default User | `nonroot`                                                                        | `nonroot`                                                                        |
| Entrypoint   | `/sbin/tini -g --`                                                               | `/sbin/tini -g --`                                                               |
| CMD          | `/usr/bin/dask-gateway-server --config /etc/dask-gateway/dask_gateway_config.py` | `/usr/bin/dask-gateway-server --config /etc/dask-gateway/dask_gateway_config.py` |
| Workdir      | not specified                                                                    | not specified                                                                    |
| Has apk?     | yes                                                                              | no                                                                               |
| Has a shell? | yes                                                                              | no                                                                               |

Check the [tags history page](/chainguard/chainguard-images/reference/dask-gateway/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                          | latest-dev | latest |
|--------------------------|------------|--------|
| `apk-tools`              | X          |        |
| `bash`                   | X          |        |
| `busybox`                | X          |        |
| `ca-certificates-bundle` | X          | X      |
| `dask-gateway`           | X          | X      |
| `gdbm`                   | X          | X      |
| `git`                    | X          |        |
| `glibc`                  | X          | X      |
| `glibc-locale-posix`     | X          | X      |
| `ld-linux`               | X          | X      |
| `libbrotlicommon1`       | X          |        |
| `libbrotlidec1`          | X          |        |
| `libbz2-1`               | X          | X      |
| `libcrypt1`              | X          | X      |
| `libcrypto3`             | X          | X      |
| `libcurl-openssl4`       | X          |        |
| `libexpat1`              | X          | X      |
| `libffi`                 | X          | X      |
| `libgcc`                 | X          | X      |
| `libidn2`                | X          |        |
| `libnghttp2-14`          | X          |        |
| `libpcre2-8-0`           | X          |        |
| `libpsl`                 | X          |        |
| `libssl3`                | X          | X      |
| `libstdc++`              | X          | X      |
| `libunistring`           | X          |        |
| `mpdecimal`              | X          | X      |
| `ncurses`                | X          | X      |
| `ncurses-terminfo-base`  | X          | X      |
| `openssl-config`         | X          | X      |
| `python-3.12`            | X          | X      |
| `readline`               | X          | X      |
| `sqlite-libs`            | X          | X      |
| `tini`                   | X          | X      |
| `wget`                   | X          |        |
| `wolfi-baselayout`       | X          | X      |
| `xz`                     | X          | X      |
| `zlib`                   | X          | X      |

