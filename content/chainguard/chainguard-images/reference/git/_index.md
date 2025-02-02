---
title: "Image Overview: git"
linktitle: "git"
type: "article"
layout: "single"
description: "Overview: git Chainguard Image"
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
{{< tab title="Overview" active=true url="/chainguard/chainguard-images/reference/git/" >}}
{{< tab title="Variants" active=false url="/chainguard/chainguard-images/reference/git/image_specs/" >}}
{{< tab title="Tags History" active=false url="/chainguard/chainguard-images/reference/git/tags_history/" >}}
{{< tab title="Provenance" active=false url="/chainguard/chainguard-images/reference/git/provenance_info/" >}}
{{</ tabs >}}



<!--overview:start-->
A minimal Git image.
<!--overview:end-->

<!--getting:start-->
## Download this Image
The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/git:latest
```
<!--getting:end-->

<!--body:start-->
Note that there is also glibc version of this Image available:

```
docker pull cgr.dev/chainguard/git:latest-glibc
```

## Usage

Chainguard's Git Image allows you to run ordinary Git commands in CI/CD pipelines and also locally via Docker.

### Docker Setup

To make sure you have the latest version of the Image available, start by running a `docker pull` command:

```shell
docker pull cgr.dev/chainguard/git
```

Then, run the Image with the `--version` flag to make sure the Image is functional:

```shell
docker run -it --rm cgr.dev/chainguard/git --version
```

You will receive output similar to this:

```
git version 2.43.0
```

### Cloning a Repository Locally

Because your local system user's unique identifier might differ from that of the container, you'll need to set up special permissions for the target directory if you want to use this Image to clone repositories locally. Once you've configured these permissions, you'll be able to set up a volume and have the contents of the cloned repository replicated on your host machine.

First, create a target directory somewhere in your home folder and set the required permissions:

```shell
mkdir ~/workspace
chmod go+wrx ~/workspace
```

Now you can use `docker run` to execute the `git clone` command, using the directory you just set up as a volume shared between your local machine and the container Image:

```shell
docker run -it -v ~/workspace:/home/git --rm cgr.dev/chainguard/git clone https://github.com/chainguard-images/.github.git
```

Here, the volume is mounted to the `/home/git` directory in the container.

This will return output like the following:

```
Cloning into '.github'...
remote: Enumerating objects: 251, done.
remote: Counting objects: 100% (33/33), done.
remote: Compressing objects: 100% (23/23), done.
remote: Total 251 (delta 15), reused 22 (delta 10), pack-reused 218
Receiving objects: 100% (251/251), 216.59 KiB | 1.04 MiB/s, done.
Resolving deltas: 100% (88/88), done.
```

You can now check the contents of your `workspace` directory, where you will find the cloned repository:

```shell
ls -a ~/workspace/
```
```
.  ..  .github
```
<!--body:end-->

