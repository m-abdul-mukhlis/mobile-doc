---
sidebar_position: 3
---

# Extras

### VSCode Snippets
```jsx title="~/.config/Code/User/snippets/typescriptreact.json"
{
  "Esoftplay hook": {
    "prefix": "eh",
    "body": [
      "// withHooks",
      "",
      "import React from 'react';",
      "import { View } from 'react-native';",
      "",
      "",
      "export interface $1Args {",
      "\t",
      "}",
      "export interface $1Props {",
      "\t",
      "}",
      "export default function m(props: $1Props): any {",
      "\treturn (",
      "\t\t<View>",
      "\t\t</View>",
      "\t)",
      "}"
    ]
  },
  "Esoftplay libs": {
    "prefix": "el",
    "body": [
      "// useLibs",
      "",
      "import React from 'react';",
      "",
      "",
      "export interface $1Props {",
      "\t",
      "}",
      "export default function m(props: $1Props): any {",
      "\treturn null",
      "}"
    ]
  }
}
```