This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

# Getting Started
### If you see error move temporary file

```bash
# using command
cd android
./gradlew clean
./gradlew --stop
```

### To install Native Dependencies ( Tailwind)
```bash
# using command
yarn add nativewind
yarn add --dev tailwindcss@3.3.2
npx tailwindcss init
```
### For default react native not support className

Create file nativewind-env.d.ts

```ts
// nativewind-env.d.ts
/// <reference types="nativewind/types" />
```
In file babel.config.js

```js
module.exports = {
   presets: ['module:@react-native/babel-preset'],
   plugins: ["nativewind/babel"] // Add this line
};
```

In file tailwind.config.js

```js
// tailwind.config.js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
# Learn More

To learn more about React Native, take a look at the following resources:

- [React Native Website](https://reactnative.dev) - learn more about React Native.
- [Getting Started](https://reactnative.dev/docs/environment-setup) - an **overview** of React Native and how setup your environment.
- [Learn the Basics](https://reactnative.dev/docs/getting-started) - a **guided tour** of the React Native **basics**.
- [Blog](https://reactnative.dev/blog) - read the latest official React Native **Blog** posts.
- [`@facebook/react-native`](https://github.com/facebook/react-native) - the Open Source; GitHub **repository** for React Native.
