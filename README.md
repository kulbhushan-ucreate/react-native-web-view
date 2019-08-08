# react-native-web-view

## Installation 
  `yarn add kulbhushan-ucreate/react-native-web-view`
          OR
  `npm install --save kulbhushan-ucreate/react-native-web-view`

## Linking 
  `react-native link react-native-webview`
  
## Usage

Import the `WebView` component from `react-native-web-view` and use it like so:

```jsx
import React, { Component } from 'react';
import { StyleSheet, Text, View, Platform } from 'react-native';
import { WebView } from 'react-native-webview';

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


