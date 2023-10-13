## Adding CSS Design 

To add a simple CSS design to your React Native app using Expo, you can use the `StyleSheet` component provided by React Native. Here's how you can modify your "Hello World" app to include some basic styling:

1. Open your `App.js` file in your text editor and update it with the following code:

```jsx
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.text}>Hello, World!</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#3498db', // Background color
  },
  text: {
    fontSize: 24,
    fontWeight: 'bold',
    color: 'white', // Text color
  },
});
```

In this updated code:

- We've added a background color to the `container` view to give it a blue background.
- We've styled the text using the `text` style, setting the font size, font weight, and text color.

2. Save your changes.

3. If your Expo development server isn't already running, start it with:

```bash
expo start
```

4. Test your app on an emulator/simulator or on a physical device as described earlier. You should now see your "Hello, World!" text displayed with the specified styles.
