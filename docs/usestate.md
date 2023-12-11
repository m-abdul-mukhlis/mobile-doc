---
sidebar_position: 3
---

# useState
Replacement for React `useState`
### Declaration
```jsx
const [state, setState, getState] = useSafeState()
```
| Name         | Type      | Description  |
| :----        | :---      | :---         |
| state        | any       | -            |
| setState     | (lastValue?:any) => void | setter function for update the state |
| getState     | () => void  | getter function for get the latest state inside function |
| useSafeState | any  | you can pass default value inside useSafeState as initial value |
