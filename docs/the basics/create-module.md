---
sidebar_position: 2
---

# Create a Module

Add **JSX** files to `modules` to create a **module**:

- `modules/main/index.tsx` --> `main` is module name and `index.tsx` is task name.

## Create your first Module
Create a file at `modules/main/index.tsx`:

```jsx title="modules/main/index.tsx"
// withHooks

import React from 'react';
import { Text, View } from 'react-native';


export interface MainIndexArgs {

}
export interface MainIndexProps {

}
export default function m(props: MainIndexProps): any {
  return (
    <View style={{ flex: 1 }}>
      <Text>HELOO WORLD</Text>
    </View>
  )
}
```

:::warning important

The names of arguments (Args) and properties (Props) are created by combining the camel case versions of folder names and file names. In this example, the folder name is `main`, and the file name is `index`.

:::

This is the result after adding new module `MainIndex`.

![helo](/img/helo.png)
