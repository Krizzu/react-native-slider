# `@react-native-community/slider`
[![CircleCI Status](https://img.shields.io/circleci/project/github/react-native-community/react-native-slider/master.svg)](https://circleci.com/gh/react-native-community/workflows/react-native-slider/tree/master) ![Supports Android and iOS](https://img.shields.io/badge/platforms-android%20|%20ios-lightgrey.svg) ![MIT License](https://img.shields.io/npm/l/@react-native-community/slider.svg)

React Native component used to select a single value from a range of values.

![iOS Screenshot](https://i.postimg.cc/dQTYzGD5/Screenshot-2019-03-25-at-11-24-59.png)
![Android Screenshot](https://i.postimg.cc/CKdtbVqc/Screenshot-2019-03-25-at-11-26-54.png)


## Getting started

`yarn add @react-native-community/slider`

or

`npm install @react-native-community/slider --save`

## React Native Compatibility
To use this library you need to ensure you are using the correct version of React Native.

| `@react-native-community/slider` version | Required React Native Version |
| ---------------------------------------- | ----------------------------- |
| `2.x.x`                                  | `>= 0.60`                     |
| [`1.x.x`](https://github.com/react-native-community/react-native-slider/tree/937f0942f1fffc6ed88b5cf7c88d73b7878f00f0)  | `<= 0.59`                     |


## Migrating from the core `react-native` module
This module was created when the Slider was split out from the core of React Native. To migrate to this module you need to follow the installation instructions above and then change you imports from:

```javascript
import { Slider } from 'react-native';
```

to:

```javascript
import Slider from '@react-native-community/slider';
```

## Usage

### Example

```javascript
import Slider from '@react-native-community/slider';
```

```javascript
  <Slider
    style={{width: 200, height: 40}}
    minimumValue={0}
    maximumValue={1}
    minimumTrackTintColor="#FFFFFF"
    maximumTrackTintColor="#000000"
  />
```

Check out the [example project](example) for more examples.

### Props

* [Inherited `View` props...](https://github.com/facebook/react-native-website/blob/master/docs/view.md#props)

- [`style`](#style)
- [`disabled`](#disabled)
- [`maximumValue`](#maximumvalue)
- [`minimumTrackTintColor`](#minimumtracktintcolor)
- [`minimumValue`](#minimumvalue)
- [`onSlidingStart`](#onslidingstart)
- [`onSlidingComplete`](#onslidingcomplete)
- [`onValueChange`](#onvaluechange)
- [`step`](#step)
- [`maximumTrackTintColor`](#maximumtracktintcolor)
- [`testID`](#testid)
- [`value`](#value)
- [`inverted`](#inverted)
- [`thumbTintColor`](#thumbtintcolor)
- [`maximumTrackImage`](#maximumtrackimage)
- [`minimumTrackImage`](#minimumtrackimage)
- [`thumbImage`](#thumbimage)
- [`trackImage`](#trackimage)

---

### `style`

Used to style and layout the `Slider`. See `StyleSheet.js` and `ViewStylePropTypes.js` for more info.

| Type       | Required |
| ---------- | -------- |
| View.style | No       |

---

### `disabled`

If true the user won't be able to move the slider. Default value is false.

| Type | Required |
| ---- | -------- |
| bool | No       |

---

### `maximumValue`

Initial maximum value of the slider. Default value is 1.

| Type   | Required |
| ------ | -------- |
| number | No       |

---

### `minimumTrackTintColor`

The color used for the track to the left of the button. Overrides the default blue gradient image on iOS.

| Type               | Required |
| ------------------ | -------- |
| [color](colors.md) | No       |

---

### `minimumValue`

Initial minimum value of the slider. Default value is 0.

| Type   | Required |
| ------ | -------- |
| number | No       |

---

### `onSlidingStart`

Callback that is called when the user picks up the slider. The initial value is passed as an argument to the callback handler.

| Type     | Required |
| -------- | -------- |
| function | No       |

---

### `onSlidingComplete`

Callback that is called when the user releases the slider, regardless if the value has changed. The current value is passed as an argument to the callback handler.

| Type     | Required |
| -------- | -------- |
| function | No       |

---

### `onValueChange`

Callback continuously called while the user is dragging the slider.

| Type     | Required |
| -------- | -------- |
| function | No       |

---

### `step`

Step value of the slider. The value should be between 0 and (maximumValue - minimumValue). Default value is 0.

| Type   | Required |
| ------ | -------- |
| number | No       |

---

### `maximumTrackTintColor`

The color used for the track to the right of the button. Overrides the default gray gradient image on iOS.

| Type               | Required |
| ------------------ | -------- |
| [color](colors.md) | No       |

---

### `testID`

Used to locate this view in UI automation tests.

| Type   | Required |
| ------ | -------- |
| string | No       |

---

### `value`

Initial value of the slider. The value should be between minimumValue and maximumValue, which default to 0 and 1 respectively. Default value is 0.

_This is not a controlled component_, you don't need to update the value during dragging.

| Type   | Required |
| ------ | -------- |
| number | No       |

---

### `inverted`
Reverses the direction of the slider. Default value is false.

| Type | Required |
| ---- | -------- |
| bool | No       |

---

### `thumbTintColor`

Color of the foreground switch grip.

| Type               | Required | Platform |
| ------------------ | -------- | -------- |
| [color](colors.md) | No       | Android  |

---

### `maximumTrackImage`

Assigns a maximum track image. Only static images are supported. The leftmost pixel of the image will be stretched to fill the track.

| Type                   | Required | Platform |
| ---------------------- | -------- | -------- |
| Image.propTypes.source | No       | iOS      |

### `minimumTrackImage`

Assigns a minimum track image. Only static images are supported. The rightmost pixel of the image will be stretched to fill the track.

| Type                   | Required | Platform |
| ---------------------- | -------- | -------- |
| Image.propTypes.source | No       | iOS      |

---

### `thumbImage`

Sets an image for the thumb. Only static images are supported.

| Type                   | Required | Platform |
| ---------------------- | -------- | -------- |
| Image.propTypes.source | No       | iOS      |

---

### `trackImage`

Assigns a single image for the track. Only static images are supported. The center pixel of the image will be stretched to fill the track.

| Type                   | Required | Platform |
| ---------------------- | -------- | -------- |
| Image.propTypes.source | No       | iOS      |

## Maintainers

- [Michał Chudziak](https://github.com/michalchudziak) - [Callstack](https://callstack.com/)

## Contributors

This module was extracted from `react-native` core. Please reffer to https://github.com/react-native-community/react-native-slider/graphs/contributors for the complete list of contributors.

## License
The library is released under the MIT licence. For more information see `LICENSE`.
