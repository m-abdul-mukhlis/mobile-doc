---
sidebar_position: 1
---

# Project Structure

### Struktur folder
```
my-app
├── app.json
├── App.tsx
├── assets
│   ├── adaptive-icon.png
│   ├── favicon.png
│   ├── icon.png
│   ├── locale
│   │   └── id.json
│   └── splash.png
├── babel.config.js
├── bun.lockb
├── config.json
├── config.live.json
├── eas.json
├── index.d.ts
├── modules
├── package.json
└── tsconfig.json
```

### Penjelasan mengenai `config.json`
```jsx title="config.json"
{
  "config": {
    "domain": "domain.com",
    "errorReport": {
      "telegramIds": [
        "xxx"
      ]
    },
    "isDebug": 0,
    "group_id": 4,
    "experienceId": "@username/slug",
    "salt": "CHANGE_INTO_YOUR_OWN_SALT",
    "home": {
      "public": "main/index",
      "member": "main/index"
    }
  }
}
```
- `domain` adalah domain dari API yg akan diakses jika aplikasi adalah aplikasi online yg menggunakan API.
- `telegramIds` untuk keperluan report error yang terjadi di aplikasi. Report akan dikirim ke id telegram yang didaftarkan.
- `isDebug` value 0 | 1 untuk menampilkan log di terminal.
- `experienceId` berisi username/slug yg terdaftar di website [Expo](http://expo.dev).
- `salt` wajib jika aplikasi terhubung ke server dengan framework `esoftplay`.
- `home` merupakan halaman atau module yang pertamakali ditampilkan saat aplikasi dijalankan. `public` untuk tampilan tanpa login dan `member` halaman untuk user yang sudah login. Default `main/index` adalah module yang berada di `node_modules`. `main/index` akan direplace jika kamu membuat module yg sama di `modules`.

