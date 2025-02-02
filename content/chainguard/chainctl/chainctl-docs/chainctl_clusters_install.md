---
date: 2024-02-20T22:23:18Z
title: "chainctl clusters install"
slug: chainctl_clusters_install
url: /chainguard/chainctl/chainctl-docs/chainctl_clusters_install/
draft: false
tags: ["chainctl", "Reference", "Product"]
images: []
type: "article"
toc: true
---
## chainctl clusters install

Install Chainguard into the current kubernetes context.

```
chainctl clusters install [--name NAME] [--description DESCRIPTION] [--parent ORGANIZATION_NAME|ORGANIZATION_NAME_ID|FOLDER_NAME|FOLDER_ID | --invite-code INVITE_CODE | --skip-invite | --cluster=CLUSTER_NAME | --private]
```

### Examples

```
  # Install or Update the chainguard agent on a cluster.
  chainctl cluster install --skip-invite
  
  # Install or Update the chainguard agent on a cluster with private API endpoint
  chainctl cluster install --private
  
  # Install the Chainguard agent with an explicit invite code.
  chainctl cluster install --invite-code=INVITE_CODE
  
  # Install the Chainguard agent using a temporary invite code under the organization
  # with ID "ORG_ID".
  chainctl cluster install --parent=ORG_ID
  
  # Install the Chainguard agent enabling a fail open policy mode.
  chainctl cluster install --opt=webhook_fail_open=true
  
  # Install the Chainguard agent using a temporary invite code under a location
  # determined via an interactive prompt.
  chainctl cluster install
```

### Options

```
      --context string                   Indicates the name of the context (in kubectl) to be connect to Chainguard.
  -d, --description string               The description of the resource.
      --gcp-serviceaccount-file string   The path to a GCP service account JSON key file.
  -h, --help                             help for install
      --invite-code string               An invite code to use for joining this cluster into the IAM hierarchy.
  -n, --name string                      Given name of the resource.
      --opt strings                      extra key=value pairs to define enforcer profile options
      --parent string                    The location under which to create a temporary invite code and install the cluster.
      --private                          Kubernetes API endpoint isn't publicly accessible.
      --profiles stringArray             The names of Chainguard profiles to install into the cluster.
      --skip-invite                      When specified we perform installation without an invite code.
```

### Options inherited from parent commands

```
      --api string        The url of the Chainguard platform API. (default "https://console-api.enforce.dev")
      --audience string   The Chainguard token audience to request. (default "https://console-api.enforce.dev")
      --config string     A specific chainctl config file. Uses CHAINCTL_CONFIG environment variable if a file is not passed explicitly.
      --console string    The url of the Chainguard platform Console. (default "https://console.enforce.dev")
      --issuer string     The url of the Chainguard STS endpoint. (default "https://issuer.enforce.dev")
  -o, --output string     Output format. One of: ["", "json", "id", "table", "terse", "tree", "wide"]
  -v, --v int             Set the log verbosity level.
```

### SEE ALSO

* [chainctl clusters](/chainguard/chainctl/chainctl-docs/chainctl_clusters/)	 - Cluster related commands for the Chainguard platform.

