react-native-radio-form-custom
================================================
  
react-native-radio-form is a simple Radio’s form, it’s a pure JS's component and it could used for the Android and iOS

![](https://github.com/cuiyueshuai/react-native-radio-form-custom/raw/master/radio-form.png)

Installation
----------------------------------------------

```bash
npm install react-native-radio-form-custom --save
```
**Note**: The radio-form is based on ECMAScript6, if you use React Native < `v0.13`, maybe it don't run


Usage
--------------------------------------------

```javascript
import React, { Component } from 'react';
import { StyleSheet, View } from 'react-native';
import RadioForm from 'react-native-radio-form-custom';
const mockData = [
    {
        label: 'label1',
        value: 'fi'
    },
    {
        label: 'label2',
        value: 'se'
    },
    {
        label: 'label3',
        value: 'th'
    }
];

export default class PRNRadioForm extends Component {

    _onSelect = ( item ) => {
      console.log(item);
    };

  render() {
    return (
      <View style={styles.container}>
        <View style={{ marginVertical: 10 }} >
         <RadioForm
              dataSource={mockData}
              itemShowKey="label"
              itemRealKey="value"
              circleSize={20}
              initial={0}
              formHorizontal={false}
              labelHorizontal={true}
              outerColor = {'#C7C7C7'}
              innerColor = {'#0D2143'}
              customTextStyle = {{fontFamily: "CenturyGothic", color: '#7C7C7C', fontSize: 14}}
              customViewStyle = {{ flex:1, padding: 2.5, flexDirection: 'row', height:50, borderColor:'#EEEEEE', backgroundColor:'#FFFFFF', alignItems: 'center', borderTopWidth:0.5, borderBottomWidth:0.5 , marginTop:-0.5, width:WINDOW_WIDTH }}
              onPress={(item) => this._onSelect(item)}
          />
        </View>
      </View>
    );
  }
}
```

Properties
-------------------------------------------

| Prop  | Default  | Type | Description |
| :------------ |:---------------:| :---------------:| :-----|
| style | - | `object` | Specify the style of the radio-form, eg. width..., but don't suggest setting height |
| dataSource | - | `array` | Specify the display date of radio-form. `array` type value must match the specified format and it's required |
|itemShowKey | 'label' | `string` | Specify the display property that radio-form's item from dataSource |
| itemRealKey | 'value' | `string` | Specify the real-selected property that radio-form's item from dataSource |
| circleSize | 20 | `number` | Specify the size of radio-form's circle |
| initial | 0 | `number | string` | Specify the initial value, it's array's index or what is itemShowKey's value and itemRealKey's |
| onPress | - | `function` | This is called when the user click the Radio's item in the UI, The first and only argument is return object from dataSource when it's called |
| formHorizontal | false | `boolean` | Specify the form whether can horizontal arrangement |
| labelHorizontal | true | `boolean` | Specify between circle and label whether can horizontal arrangement |
| outerColor | '#2f86d5' | `string` |  Specify the color the radio-form's outer-circle |
| innerColor | '#2f86d5' | `string` |  Specify the color the radio-form's center point |


Licence
-------------------------------------------

(MIT)


