---
date: 2024-02-20T22:23:18Z
title: "chainctl iam role-bindings list"
slug: chainctl_iam_role-bindings_list
url: /chainguard/chainctl/chainctl-docs/chainctl_iam_role-bindings_list/
draft: false
tags: ["chainctl", "Reference", "Product"]
images: []
type: "article"
toc: true
---
## chainctl iam role-bindings list

List role-bindings.

```
chainctl iam role-bindings list [--parent ORGANIZATION_NAME | ORGANIZATION_ID | FOLDER_NAME | FOLDER_ID] [--output table|tree|json]
```

### Examples

```
  # List role-bindings
  chainctl iam role-bindings list
  
  # Filter role-bindings by organization
  chainctl iam role-bindings list --parent=my-org
```

### Options

```
  -h, --help            help for list
      --parent string   List role-bindings from this location.
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

* [chainctl iam role-bindings](/chainguard/chainctl/chainctl-docs/chainctl_iam_role-bindings/)	 - IAM role-bindings resource interactions.

