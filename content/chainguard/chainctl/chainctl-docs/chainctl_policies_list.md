---
date: 2024-02-20T22:23:18Z
title: "chainctl policies list"
slug: chainctl_policies_list
url: /chainguard/chainctl/chainctl-docs/chainctl_policies_list/
draft: false
tags: ["chainctl", "Reference", "Product"]
images: []
type: "article"
toc: true
---
## chainctl policies list

List policies.

```
chainctl policies list [--parent ORGANIZATION_NAME | ORGANIZATION_ID | FOLDER_NAME | FOLDER_ID] [--image=IMAGE] [--output table|json|id]
```

### Examples

```
  # List all policies in the "eng" organization
  chainctl policy list --parent=eng
  
  # List all policies the user has permission to view
  chainctl policy list
```

### Options

```
  -h, --help            help for list
      --image string    The name of an image to filter the results.
      --parent string   The name or id of the parent location to list policies from.
  -y, --yes             Automatic yes to prompts; assume "yes" as answer to all prompts and run non-interactively.
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

