---
sidebar_position: 1
---

# Installation
Let's discover **Esoftplay Mobile in less than 5 minutes**.

## Getting Started
Get started by **creating a new expo project**.

### What you'll need
- [Node.js LTS](https://nodejs.org/en/download/) version 16.0 or above. Or using [NVM (Node Version Manager)](https://github.com/nvm-sh/nvm) for quickly install and use different vesion of node.
- [Watchman](https://facebook.github.io/watchman/) use version 4.9.0.
- [Visual Studio Code](https://code.visualstudio.com/download) or use other text editor.
- Curl
- Git

### Preparation
Installing bun:
```bash
npm install -g bun
```
Installing yarn:
```bash
npm install -g yarn
```
Installing esoftplay-cli:
```bash
npm install -g esoftplay-cli
```
Installing typescript:
```bash
npm install -g typescript
```
Installing eas-cli:
```bash
npm install -g eas-cli
```

## Create a new project
Create new expo project:

replace my-app with your app name.

```bash
npx create-expo-app my-app --template expo-template-blank-typescript@sdk-48
```
```bash
cd my-app
```
```bash
bun add esoftplay && bun install
```

`./package.json` file will look like this when installation is success:

```jsx title="package.json"
{
  "name": "my-app",
  "version": "1.0.0",
  "main": "node_modules/expo/AppEntry.js",
  "scripts": {
    "start": "esp start && npx expo start --dev-client",
    "android": "expo start --android",
    "ios": "expo start --ios",
    "web": "expo start --web"
  },
  "dependencies": {
    "@expo/vector-icons": "^13.0.0",
    "@react-native-async-storage/async-storage": "^1.17.11",
    "@react-native-community/netinfo": "^9.3.7",
    "@react-native-masked-view/masked-view": "^0.2.8",
    "@react-navigation/native": "^6.1.9",
    "@react-navigation/native-stack": "^6.9.17",
    "@react-navigation/stack": "^6.3.20",
    "@shopify/flash-list": "1.4.0",
    "buffer": "^6.0.3",
    "dayjs": "^1.11.10",
    "esoftplay": "^0.0.135-z",
    "expo": "~48.0.21",
    "expo-application": "~5.1.1",
    "expo-camera": "~13.2.1",
    "expo-clipboard": "~4.1.2",
    "expo-constants": "~14.2.1",
    "expo-dev-client": "~2.2.1",
    "expo-document-picker": "~11.2.2",
    "expo-file-system": "~15.2.2",
    "expo-font": "~11.1.1",
    "expo-image-manipulator": "~11.1.1",
    "expo-image-picker": "~14.1.1",
    "expo-linear-gradient": "~12.1.2",
    "expo-media-library": "~15.2.3",
    "expo-notifications": "~0.18.1",
    "expo-secure-store": "~12.1.1",
    "expo-splash-screen": "~0.18.2",
    "expo-status-bar": "~1.4.4",
    "expo-updates": "~0.16.4",
    "immhelper": "^1.0.52",
    "react": "18.2.0",
    "react-fast-compare": "^3.2.0",
    "react-native": "0.71.8",
    "react-native-awesome-gallery": "0.3.5",
    "react-native-calendar-picker": "^7.1.2",
    "react-native-chart-kit": "^6.11.0",
    "react-native-fast-image": "^8.5.11",
    "react-native-gesture-handler": "~2.9.0",
    "react-native-maps": "1.3.2",
    "react-native-mmkv": "^2.10.2",
    "react-native-pan-pinch-view": "^1.0.1",
    "react-native-pinch-zoom-view-movable": "^0.2.1",
    "react-native-qrcode-svg": "^6.0.1",
    "react-native-reanimated": "~2.14.4",
    "react-native-render-html": "^6.3.4",
    "react-native-safe-area-context": "4.5.0",
    "react-native-screens": "~3.20.0",
    "react-native-screenshot-prevent": "1.1.1",
    "react-native-svg": "13.4.0",
    "react-native-view-shot": "3.5.0",
    "react-native-web": "~0.18.11",
    "react-native-webview": "11.26.0",
    "shorthash": "^0.0.2",
    "usestable": "^0.1.25"
  },
  "devDependencies": {
    "@babel/core": "^7.20.0",
    "@types/react": "~18.0.14",
    "typescript": "^4.9.4"
  },
  "private": true,
  "trustedDependencies": [
    "esoftplay",
    "esoftplay-android-print",
    "esoftplay-chatting",
    "esoftplay-firestore",
    "esoftplay-content",
    "esoftplay-lib-print",
    "esoftplay-log",
    "esoftplay-market",
    "esoftplay-ppob",
    "esoftplay-web",
    "esoftplay-web-pwa"
  ]
}
```

If the installation fails and the `package.json` only contains the `esoftplay` package under dependencies, you can manually install the missing dependencies using the following commands:

```bash
npx expo install expo-application expo-camera expo-clipboard expo-constants expo-document-picker expo-dev-client expo-file-system expo-font expo-image-manipulator expo-image-picker expo-linear-gradient expo-media-library expo-notifications expo-status-bar expo-splash-screen expo-secure-store expo-updates
```
and

```bash
yarn add @expo/vector-icons @react-native-async-storage/async-storage @react-native-masked-view/masked-view @react-native-community/netinfo @react-navigation/native-stack @react-navigation/native @react-navigation/stack @shopify/flash-list buffer immhelper dayjs react-fast-compare react-native-gesture-handler react-native-awesome-gallery react-native-fast-image react-native-mmkv react-native-pan-pinch-view react-native-reanimated react-native-safe-area-context react-native-screens react-native-webview shorthash usestable
```

:::tip Tip
If failed you can install it one-by-one.
:::

## Start your app
Before starting your app, you need to add this following bash script to your `~/.bashrc`.
```bash
alias wfix='watchman watch-del-all && bun start'
alias reinstall='rm -rf node_modules package-lock.json yarn.lock bun.lockb && bun install && wfix'
alias cleaninstall='rm -rf node_modules package-lock.json yarn.lock bun.lockb ~/.bun/install/cache && bun install && wfix'
```

After add that script to your `~/.bashrc` you need to reload your `~/.bashrc` for change to be applied. Just close your opened terminal and then open new terminal or use this script:
```bash
. ~/.bashrc
```

To start your app, open the terminal, navigate to the directory where your project is located using the `cd` command, and then execute `bun start`

```bash
cd /my-app
bun start
```

This is the first look page after successfully start the app.

![firstlook](/img/firstlook.png)

:::tip Pro-Tip

If you encounter issues starting your app or discover any missing dependencies, simply run `cleaninstall` or `reinstall`.

:::