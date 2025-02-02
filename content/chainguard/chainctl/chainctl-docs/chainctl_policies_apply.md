---
date: 2024-02-20T22:23:18Z
title: "chainctl policies apply"
slug: chainctl_policies_apply
url: /chainguard/chainctl/chainctl-docs/chainctl_policies_apply/
draft: false
tags: ["chainctl", "Reference", "Product"]
images: []
type: "article"
toc: true
---
## chainctl policies apply

Create or update a policy described by file or stdin.

```
chainctl policies apply [--parent ORGANIZATION_NAME | ORGANIZATION_ID | FOLDER_NAME | FOLDER_ID] [--description=DESCRIPTION] [--filename=FILENAME]... [--recursive] [--yes] [--output table|json|id]
```

### Examples

```
  # Apply a policy document from disk to the "eng" organization
  chainctl policy apply --filename=images-are-signed.yaml --parent=eng
  
  # Apply an updated policy document to an existing policy, automatically respond yes to confirmation prompts
  chainctl policy apply -f images-are-signed-v2.yaml --parent=eng --yes
  
  # Apply a policy document from stdin, interactively choose the location to apply the policy to
  chainctl policy apply -f -
```

### Options

```
  -d, --description string   The description of the policy.
  -f, --filename strings     Filename, directory, or URL to files to use to create or update the resource
  -h, --help                 help for apply
      --parent string        The parent location name or id of the policy.
  -R, --recursive            Process the directory used in -f, --filename recursively. Useful when you want to manage related manifests organized within the same directory.
  -y, --yes                  Automatic yes to prompts; assume "yes" as answer to all prompts and run non-interactively.
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

* [chainctl policies](/chainguard/chainctl/chainctl-docs/chainctl_policies/)	 - Policy related commands for the Chainguard platform.

