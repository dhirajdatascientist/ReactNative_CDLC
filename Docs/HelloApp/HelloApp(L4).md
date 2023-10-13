## Problem Statement
The next feature we can add to our React Native app is navigation between multiple screens using React Navigation. This will allow us to create a simple multi-screen app. Here are the steps to add navigation:

1. Install React Navigation and its dependencies if you haven't already. Open your terminal and run:

```bash
npm install @react-navigation/native @react-navigation/stack react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/viewpager
```

2. Now, you need to set up navigation in your app. Update your `App.js` file as follows:

```jsx
import React from 'react';
import { NavigationContainer } from '@react-navigation/native';
import { createStackNavigator } from '@react-navigation/stack';
import HomeScreen from './screens/HomeScreen';
import SecondScreen from './screens/SecondScreen';

const Stack = createStackNavigator();

export default function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Second" component={SecondScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
```

In this code:

- We import the necessary modules from React Navigation.
- We create a `Stack.Navigator` that defines the navigation stack.
- We define two screens, "Home" and "Second," and associate them with components `HomeScreen` and `SecondScreen`, respectively.

3. Create two new files `HomeScreen.js` and `SecondScreen.js` in the same directory as your `App.js` file, and add the following code to each file:

`HomeScreen.js`:

```jsx
import React from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';

export default function HomeScreen({ navigation }) {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Home Screen</Text>
      <Button
        title="Go to Second Screen"
        onPress={() => navigation.navigate('Second')}
      />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#3498db',
  },
  text: {
    fontSize: 24,
    fontWeight: 'bold',
    color: 'white',
  },
});
```

`SecondScreen.js`:

```jsx
import React from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';

export default function SecondScreen({ navigation }) {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Second Screen</Text>
      <Button
        title="Go back to Home"
        onPress={() => navigation.navigate('Home')}
      />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#e74c3c',
  },
  text: {
    fontSize: 24,
    fontWeight: 'bold',
    color: 'white',
  },
});
```

4. Save your changes.

5. Start your Expo development server if it's not already running:

```bash
expo start
```

6. Test your app on an emulator/simulator or on a physical device. You should now have a navigation system in place, with a "Home Screen" and a "Second Screen." Press the buttons to navigate between the screens.
