## Problem Statement
To add another simple feature, let's add a button to our React Native app that changes the text when pressed. Here are the steps to do that:

1. Open your `App.js` file and update it with the following code:

```jsx
import React, { useState } from 'react';
import { View, Text, StyleSheet, Button } from 'react-native';

export default function App() {
  const [displayText, setDisplayText] = useState('Hello, World!');

  const changeText = () => {
    setDisplayText('Button Pressed!');
  };

  return (
    <View style={styles.container}>
      <Text style={styles.text}>{displayText}</Text>
      <Button title="Press Me" onPress={changeText} />
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

In this code:

- We've added a `useState` hook to manage the text displayed in the `displayText` variable.
- We've added a `changeText` function that updates the `displayText` state when the button is pressed.
- We've included a `<Button>` component that triggers the `changeText` function when pressed.

2. Save your changes.

3. Start your Expo development server if it's not already running:

```bash
expo start
```

4. Test your app on an emulator/simulator or on a physical device. You should now see your "Hello, World!" text displayed with a button below it. When you press the button, the text will change to "Button Pressed!"

This is a simple example of how you can add interactivity to your React Native app by updating the state when a button is pressed. You can further enhance your app by adding more features and components as needed.