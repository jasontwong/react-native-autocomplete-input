# react-native-autocomplete-input [![npm version](https://badge.fury.io/js/react-native-autocomplete-input.svg)](https://badge.fury.io/js/react-native-autocomplete-input)
This is a pure javascript react-native component to display  autocomplete suggestions given an array of objects respective to the input text.

![Autocomplete Example](https://raw.githubusercontent.com/l-urence/react-native-autocomplete-input/master/example.gif)

## How to use react-native-autocomplete-input
Fist things first install the component from npmjs.org:

```shell
$ npm install --save react-native-autocomplete-input
```

or install HEAD from github.com:

```shell
$ npm install --save l-urence/react-native-autocomplete-input
```

This brief example should illustrate the usage of the autocomplete:

```javascript
// ...
render() { 
  const { query } = this.state;
  const data = this._filterData(query)
  <Autocomplete
    data={data}
    defaultValue={query}
    onChangeText={text => this.setState({query: text})}
    renderItem={data => (
      <TouchableOpacity onPress={() => 
          this.setState({query: data})
        }
      >
        <Text>{data}</Text>
      </TouchableOpacity>
    )}
  />
}
// ... 
```

The full example from the screenshot can be found [here](https://github.com/l-urence/react-native-autocomplete-input/blob/master/example/Example.js)

## react-native-autocomplete-input props
| Prop | Type | Description |
:------------ |:---------------:| :-----|
| containerStyle | style | These styles will be applied to the container which surrounds the autocomplete component. |
| inputContainerStyle | style | These styles will be applied to the container which surrounds the textInput component. |
| style | style | These styles will be applied to the textInput component. |
| data | array | Assign an array of data objects which should be rendered in respect to the entered text. |
| listStyle | style | These style will be applied to the result list view. |
| renderItem | function | `renderItem` will be called to render the data objects which will be displayed in the result view below the text input. |


## Contribute
Feel free to open issues or do a PR!
