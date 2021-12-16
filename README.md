# vue-mzc-loading
Simple Vue2 loading component

![](demo.gif)

[Online demo](https://codesandbox.io/s/awesome-silence-5uht0?file=/src/App.vue)

## Installation
```sh
npm install vue-mzc-loading --save
```

## Usage
```js
import VueMzcLoading from "vue-mzc-loading";

export default {
  components: {
    VueMzcLoading,
  },
};
```
```html
<vue-mzc-loading
  size="48px"
  width="8px"
  color="#539bf5"
  title="Custom loading..."
/>
```