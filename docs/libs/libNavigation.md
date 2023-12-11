---
sidebar_position: 1
---

# libNavigation
Navigation and Routing for Mobile Esoftplay

### Navigate to Another Screen
```jsx
LibNavigation.navigate('module-name/task-name')
```
#### ```LibNavigation.navigate(route, params)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| route     | `string`  | module/task  |
| params<br/>`(optional)` | `any` | parameter yang ingin dibawa ke halaman tujuan |


### Navigate from A to B and get value from B
- Navigation on Sceen A
```jsx
LibNavigation.navigateForResult('module-name/task-name').then((result)=>{
  console.log(result, "value from B")
})
```
#### ```LibNavigation.navigateForResult(route, params, key)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| route     | `string`  | module/task  |
| params<br/>`(optional)` | `any` | parameter yang ingin dibawa ke halaman tujuan |
| key<br/>`(optional)`   | `number` | key sebagai pembeda tujuan |


- Navigation on Sceen B
```jsx
LibNavigation.sendBackResult(result)
```
#### ```LibNavigation.sendBackResult(result, key)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| result     | `any`  | hasil yang akan dikembalikan ke halaman sebelumnya  |
| key<br/>`(optional)`   | `number` | key sebagai pembeda tujuan |


you need to add `cancelBackResult` on `useEffect` in sceen B.
```jsx
useEffect(() => {
  LibNavigation.cancelBackResult()
}, [])
```
#### ```LibNavigation.cancelBackResult(key)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| key<br/>`(optional)`   | `number` | key sebagai pembeda tujuan |

#### ```LibNavigation.getResultKey(props)```
Digunakan untuk mendapatkan `key` yang dikirim ke halaman ini.
Dapat digunakan untuk mengisi `key` di `LibNavigation.cancelBackResult(key)` atau `LibNavigation.sendBackResult(result, key)`

key dapat diganti dengan `LibNavigation.getResultKey(props)`.


### Back from B to A
```jsx
LibNavigation.back()
```
#### ```LibNavigation.back(deep)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| deep<br/>`(optional)`      | `number`    | number of screen to be close |


### Back to Root of APP
```jsx
LibNavigation.backToRoot()
```
Digunakan untuk kembali ke halaman utama saat aplikasi dibuka. Sesuai dengan file `config.json` pada index `home`.


### Navigate with Push
`Push` membuka halaman baru. Dapat digunakan untuk navigasi ke halaman yang sama berulang-ulang tanpa menutup halaman yang sudah dibuka.
#### ```LibNavigation.push(route, params)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| route     | `string`  | module/task  |
| params<br/>`(optional)` | `any` | parameter yang ingin dibawa ke halaman tujuan |


### Mengganti halaman
`Replace` dapat digunakan untuk me-replace halaman yang saat ini dibuka
#### ```LibNavigation.replace(route, params)```
| Name      | Type      | Description  |
| :----:    | :---      | :---         |
| route     | `string`  | module/task  |
| params<br/>`(optional)` | `any` | parameter yang ingin dibawa ke halaman tujuan |
