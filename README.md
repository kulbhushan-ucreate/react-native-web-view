# react-native-web-view

## Usage

Import the `WebView` component from `react-native-web-view` and use it like so:

```jsx
import React, { Component } from 'react';
import { StyleSheet, Text, View, Platform } from 'react-native';
import { WebView } from 'react-native-web-view';

// ...
class MyWebComponent extends Component {
   onShouldStartLoadWithRequest = (request) => {
    console.log(request.url);
    if(Platform.OS === 'ios') return true;
   }
  render() {
    return (
      <WebView source={{ uri: 'https://facebook.github.io/react-native/' }} 
         onShouldStartLoadWithRequest={this.onShouldStartLoadWithRequest}
      />
    );
  }
}
```

## License

MIT


