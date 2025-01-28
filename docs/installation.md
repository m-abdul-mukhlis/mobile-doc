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
npx create-expo-app@latest --template blank-typescript
```
```bash
cd my-app
```
```bash
bun add esoftplay && bun install
```
```bash
reinstall
```

`./package.json` file will look like this when installation is success:

```jsx title="package.json"
{
  "name": "myapp",
  "version": "1.0.0",
  "main": "expo/AppEntry.js",
  "scripts": {
    "start": "esp start && bunx expo start --dev-client",
    "android": "expo start --android",
    "ios": "expo start --ios",
    "web": "expo start --web"
  },
  "dependencies": {
    "@expo/vector-icons": "^14.0.3",
    "@react-native-async-storage/async-storage": "1.23.1",
    "@react-native-community/netinfo": "11.3.1",
    "@react-native-masked-view/masked-view": "0.3.1",
    "@react-navigation/native": "^6.1.18",
    "@react-navigation/native-stack": "^6.11.0",
    "@react-navigation/stack": "^6.4.1",
    "@shopify/flash-list": "1.6.4",
    "esoftplay": "^0.0.141-r",
    "expo": "~51.0.28",
    "expo-application": "~5.9.1",
    "expo-camera": "~15.0.16",
    "expo-clipboard": "~6.0.3",
    "expo-dev-client": "~4.0.28",
    "expo-document-picker": "~12.0.2",
    "expo-image": "~1.13.0",
    "expo-image-manipulator": "~12.0.5",
    "expo-image-picker": "~15.0.7",
    "expo-linear-gradient": "~13.0.2",
    "expo-media-library": "~16.0.5",
    "expo-notifications": "~0.28.19",
    "expo-secure-store": "~13.0.2",
    "expo-splash-screen": "~0.27.6",
    "expo-sqlite": "~14.0.6",
    "expo-status-bar": "~1.12.1",
    "expo-updates": "~0.25.27",
    "immhelper": "^1.0.52",
    "react": "18.2.0",
    "react-fast-compare": "^3.2.2",
    "react-native": "0.74.5",
    "react-native-awesome-gallery": "^0.4.3",
    "react-native-gesture-handler": "~2.16.1",
    "react-native-keyboard-controller": "^1.14.2",
    "react-native-mmkv": "^3.1.0",
    "react-native-pan-pinch-view": "^2.0.0",
    "react-native-reanimated": "~3.10.1",
    "react-native-safe-area-context": "4.10.5",
    "react-native-screens": "3.31.1",
    "react-native-webview": "13.8.6",
    "shorthash": "^0.0.2",
    "usestable": "^0.1.25"
  },
  "devDependencies": {
    "@babel/core": "^7.20.0",
    "@types/react": "~18.2.45",
    "typescript": "^5.1.3"
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

<!-- ![firstlook](/img/firstlook.png) -->

:::tip Pro-Tip

If you encounter issues starting your app or discover any missing dependencies, simply run `cleaninstall` or `reinstall`.

:::