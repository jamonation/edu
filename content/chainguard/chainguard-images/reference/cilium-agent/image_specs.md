---
title: "cilium-agent Image Variants"
type: "article"
unlisted: true
description: "Detailed information about the public cilium-agent Chainguard Image variants"
date: 2023-03-07T11:07:52+02:00
lastmod: 2024-01-19 00:16:42
draft: false
tags: ["Reference", "Chainguard Images", "Product"]
images: []
weight: 550
toc: true
---

{{< tabs >}}
{{< tab title="Overview" active=false url="/chainguard/chainguard-images/reference/cilium-agent/" >}}
{{< tab title="Variants" active=true url="/chainguard/chainguard-images/reference/cilium-agent/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/cilium-agent/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/cilium-agent/provenance_info/" >}}
{{</ tabs >}}

This page shows detailed information about all public variants of the Chainguard **cilium-agent** Image.

## Variants Compared
The **cilium-agent** Chainguard Image currently has 2 public variants: 

- `latest-dev`
- `latest`

The table has detailed information about each of these variants.

|              | latest-dev              | latest                  |
|--------------|-------------------------|-------------------------|
| Default User | `root`                  | `root`                  |
| Entrypoint   | `/usr/bin/cilium-agent` | `/usr/bin/cilium-agent` |
| CMD          | not specified           | not specified           |
| Workdir      | not specified           | not specified           |
| Has apk?     | yes                     | no                      |
| Has a shell? | yes                     | yes                     |

Check the [tags history page](/chainguard/chainguard-images/reference/cilium-agent/tags_history/) for the full list of available tags.

## Packages Included
The table shows package distribution across variants.

|                                | latest-dev | latest |
|--------------------------------|------------|--------|
| `apk-tools`                    | X          |        |
| `bash`                         | X          | X      |
| `bpftool`                      | X          | X      |
| `busybox`                      | X          | X      |
| `ca-certificates-bundle`       | X          | X      |
| `cilium`                       | X          | X      |
| `cilium-container-init`        | X          | X      |
| `cilium-container-init-compat` | X          | X      |
| `cilium-envoy`                 | X          | X      |
| `clang-15`                     | X          | X      |
| `clang-15-default`             | X          | X      |
| `cni-plugins-loopback`         | X          | X      |
| `cni-plugins-main`             | X          | X      |
| `git`                          | X          |        |
| `glibc`                        | X          | X      |
| `glibc-locale-posix`           | X          | X      |
| `gops`                         | X          | X      |
| `iproute2`                     | X          | X      |
| `ipset`                        | X          | X      |
| `iptables`                     | X          | X      |
| `kmod`                         | X          | X      |
| `ld-linux`                     | X          | X      |
| `libLLVM-15`                   | X          | X      |
| `libblkid`                     | X          | X      |
| `libbrotlicommon1`             | X          |        |
| `libbrotlidec1`                | X          |        |
| `libbz2-1`                     | X          | X      |
| `libclang-cpp-15`              | X          | X      |
| `libcrypt1`                    | X          | X      |
| `libcrypto3`                   | X          | X      |
| `libcurl-openssl4`             | X          |        |
| `libelf`                       | X          | X      |
| `libexpat1`                    | X          |        |
| `libfdisk`                     | X          | X      |
| `libffi`                       | X          | X      |
| `libgcc`                       | X          | X      |
| `libidn2`                      | X          |        |
| `libmnl`                       | X          | X      |
| `libmount`                     | X          | X      |
| `libnftnl`                     | X          | X      |
| `libnghttp2-14`                | X          |        |
| `libpcre2-8-0`                 | X          |        |
| `libpsl`                       | X          |        |
| `libsmartcols`                 | X          | X      |
| `libssl3`                      | X          |        |
| `libstdc++`                    | X          | X      |
| `libunistring`                 | X          |        |
| `libuuid`                      | X          | X      |
| `libxml2`                      | X          | X      |
| `libzstd1`                     | X          | X      |
| `llvm15`                       | X          | X      |
| `llvm15-tools`                 | X          | X      |
| `mount`                        | X          | X      |
| `ncurses`                      | X          | X      |
| `ncurses-terminfo-base`        | X          | X      |
| `openssl-config`               | X          | X      |
| `util-linux-misc`              | X          | X      |
| `wolfi-baselayout`             | X          | X      |
| `xz`                           | X          | X      |
| `zlib`                         | X          | X      |

