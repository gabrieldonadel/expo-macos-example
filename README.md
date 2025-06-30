# Expo macOS Example

This repository demonstrates how to set up a React Native project with Expo and macOS support. You can follow these instruction by looking ath the commits in this repository.

1. **Initialize a new React Native project:**

   ```bash
   npx react-native init <YourProjectName>
   ```

2. **Add macOS support:**

   ```bash
   npx react-native-macos-init
   ```

   **(Optionally)** Delete `android` and `ios` folders if you only want to support macOS.

4. **Install Expo:**

   ```bash
   npm install expo
   ```

5. Using Expo CLI

   Update `package.json` to invoke Expo CLI:

    ```json
    {
      "scripts": {
        "start": "expo start",
      }
    }
    ```

   Configure `metro.config.js`

   Add the following code to your `metro.config.js` file:

   ```js
   const { getDefaultConfig } = require('expo/metro-config');

   const config = getDefaultConfig(__dirname);

   module.exports = config;
   ```

   Replace the contents of `index.js` with the following:

    ```js
    import { registerRootComponent } from 'expo';

    import App from './App';

    registerRootComponent(App);
    ```