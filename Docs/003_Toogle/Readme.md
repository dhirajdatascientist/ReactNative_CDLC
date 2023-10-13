# Task where users can toggle a piece of text between "Hello" and "World" upon clicking a button. 

```jsx
import React, { useState } from 'react';
import { StyleSheet, Text, View, Button } from 'react-native';
import { StatusBar } from 'expo-status-bar';

export default function App() {
  const [message, setMessage] = useState('Hello');

  const toggleMessage = () => {
    setMessage(prevMessage => (prevMessage === 'Hello' ? 'World' : 'Hello'));
  };

  return (
    <View style={styles.container}>
      <Text style={styles.text}>{message}</Text>
      <Button title="Toggle Message" onPress={toggleMessage} />
      <StatusBar style="auto" />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    alignItems: 'center',
    justifyContent: 'center',
  },
  text: {
    fontSize: 30,
    marginBottom: 20,
  }
});
```
In this code:

- **useState**: We create a piece of state `message` which is initially set to "Hello".
  
- **toggleMessage**: This is a function that toggles the `message` state between "Hello" and "World" each time it is called.

- **Button**: The Button component has an `onPress` prop which calls `toggleMessage` function each time it is pressed.

When you press the button, the message should toggle between "Hello" and "World" on the screen. This task involves basic state management and handling user interaction in React Native.