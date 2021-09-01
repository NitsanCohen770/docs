---
title: External Dependencies
id: external-dependencies
---

External dependencies are either Components or packages, defined in your Workspace's [Dependency Policy](/dependencies/policy), installed and resolved from the [node_modules](/workspace/node_modules) directory. 

External dependencies configured in your Workspace Dependency Policy are allowed to use from [Workspace Components](/workspace/workspace-component)

They can be used through the [`bit install`](/dependencies/commands/install) command which uses the configured [Package Manager](/dependencies/package-managers) to install the requested dependency in the [node_modules](/workspace/node-modules) directory in your [Workspace](/workspace/overview).

```bash
bit install # makes sure your workspace is up to date.
bit install @teambit/base-ui.button # adds @teambit/base-ui.button
```

External dependencies allowed to use in your Workspace can be defined in the [Dependency Policy](/dependencies/policy) in your [Workspace configuration](/workspace/config). `bit install` makes sure all external dependencies are 

// bit use adds an external dependency to be in the Dependency Policy of your Workspace and invokes `bit install`.


## Package dependencies

## Component dependencies


```json
{
  "name": "@teambit/base-ui.button",
  "componentId": "teambit.base-ui/button"
}
```