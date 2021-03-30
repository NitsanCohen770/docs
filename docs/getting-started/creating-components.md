---
id: creating-components
title: Creating Components
---

import ReactEnvironment from '@site/docs/components/workspace/react-environment.md'
import ExampleButton from '@site/docs/components/examples/button.md'

Once you have [initialize a Bit workspace](/getting-started/initializing-workspace) you can then:

1. Configure the `teambit.react/react` workspace variant to use the React example component
2. Use `bit create` to create an example component and add it to the workspace
3. Use `bit install` to install dependencies for Testing Library and Chai

Alternatively you can manually create your component files and then use `bit add` to track them.

## Setting a React Environment

<ReactEnvironment />

## Use Bit Create

We can use `bit create` to create an example button component with the namespace of `ui/button`. This will also create a package in your workspace `node_modules` directory and add your component to the workspace UI.

```sh
bit create react-example-button ui/button
```

The following files will have been created for you:

<ExampleButton />

The example component has no styles added to it. Feel free to add your a css/scss file and import it into your component's tsx file.

## Bitmap File

After adding a component the `.bitmap` file will be regenerated to show the added component. For now the scope and version will be empty.

```json
/* THIS IS A BIT-AUTO-GENERATED FILE. DO NOT EDIT THIS FILE DIRECTLY. */

{
  "ui/button": {
    "scope": "",
    "version": "",
    "mainFile": "index.ts",
    "rootDir": "button"
  },
  "version": "1.0.39"
}
```

## Install Dependencies

As we had added a test file that includes dependencies for Testing Library and Chai we will need to install them:

```sh
bit install @testing-library/react chai
```

## Show Component

We can use the `bit show` command followed by our ComponentID to see all details about our component including the env, the files and the dependencies.

```shell
bit show ui/button
```

```shell
  ┌───────────────────┬───────────────────────────────────────────────────────────────────────────────────┐
  │ id                │ my-scope/ui/button                                                                │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ scope             │ my-scope                                                                          │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ name              │ ui/button                                                                         │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ env               │ teambit.harmony/node                                                              │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ package name      │ @my-scope/ui.button                                                               │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ main file         │ index.ts                                                                          │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ files             │ button.composition.tsx                                                            │
  │                   │ button.docs.mdx                                                                   │
  │                   │ button.tsx                                                                        │
  │                   │ index.ts                                                                          │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ dev files         │ button.docs.mdx (teambit.docs/docs)                                               │
  │                   │ button.composition.tsx (teambit.compositions/compositions)                        │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ extensions        │ teambit.component/dev-files                                                       │
  │                   │ teambit.compositions/compositions                                                 │
  │                   │ teambit.pkg/pkg                                                                   │
  │                   │ teambit.docs/docs                                                                 │
  │                   │ teambit.envs/envs                                                                 │
  │                   │ teambit.dependencies/dependency-resolver                                          │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ dependencies      │                                                                                   │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ dev dependencies  │ @types/jest@26.0.20- (package)                                                    │
  ├───────────────────┼───────────────────────────────────────────────────────────────────────────────────┤
  │ peer dependencies │ react@16.13.1- (package)                                                          │
  └───────────────────┴───────────────────────────────────────────────────────────────────────────────────┘
```

## What's Next?

Once you have created and added your component to the workspace the next step is to [render the Workspace UI](workspace-ui) so you can see the component locally.