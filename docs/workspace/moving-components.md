---
title: Moving Components
id: moving-components
---

To move a component you can use the `bit move` command. This command will move the component from the current directory to the new directory.

```bash
bit move ui/my-component design/my-component
```

:::tip Move v Remove Components
This will only affect how your components are ordered in your workspace and not in your `.bitmap` file. If you want to move a component to a different namespace you will need to first remove it and then add it again with the correct namespace.
:::