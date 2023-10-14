# FirstApp Setup in React Native using Expo 

1. Install Expo CLI (if not already installed):
   If you haven't installed Expo CLI, you can do so globally using npm or yarn:
   *First_Time*

   ```bash
   npm install -g expo-cli
   # or
   yarn global add expo-cli
   ```

2. Create a new React Native project with Expo:

   ```bash
   expo init HelloWorldApp
   ```

* Follow the prompts to configure your project. 
* You can choose a blank template for this "Hello World" example.

3. Change to the project directory:

   ```bash
   cd HelloWorldApp
   ```

4. Open the `App.js` file in your text editor of choice and replace its contents with the following code:

   ```jsx
   import React from 'react';
   import { View, Text, StyleSheet } from 'react-native';

   export default function App() {
     return (
       <View style={styles.container}>
         <Text>Hello, World!</Text>
       </View>
     );
   }

   const styles = StyleSheet.create({
     container: {
       flex: 1,
       justifyContent: 'center',
       alignItems: 'center',
     },
   });
   ```

* This code defines a simple React Native component that displays "Hello, World!" in the center of the screen.

5. Run your Expo development server:

   ```bash
   expo start
   ```

* This command will start the development server and open a new browser window with the Expo DevTools.

6. You can run your app on an iOS or Android simulator/emulator, or you can scan the QR code displayed in the terminal with the Expo Go app on your physical device to see the app in action.
