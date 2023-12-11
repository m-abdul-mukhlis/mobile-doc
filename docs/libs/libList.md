---
sidebar_position: 2
---

# libList
List View for Mobile Esoftplay

## Simple Usage
```jsx
const data = new Array(10).fill(" ")
return (
  <View style={{ flex: 1 }}>
    <LibList
      data={data}
      renderItem={(item: any, index: number) => (
        <Text>{index}</Text>
      )}
    />
  </View>
)
```
## Props
### data `(required)`
An array (or array-like list) of items to render. Other data types can be used by targetting VirtualizedList directly.

### renderItem `(required)`
```jsx
renderItem: (item: any, index: number) => any
```
- `item` (Object): The item from data being rendered.
- `index` (number): The index corresponding to this item in the data array.