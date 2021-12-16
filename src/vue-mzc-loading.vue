<script>
export default /*#__PURE__*/ {
  name: "VueMzcLoading", // vue component name
  props: {
    title: {
      type: String,
      default: "",
    },
    size: {
      type: String,
      default: "24px",
    },
    width: {
      type: String,
      default: "2px",
    },
    color: {
      type: String,
      default: "currentColor",
    },
  },
};
</script>

<template>
  <div class="vue-mzc-loading">
    <div
      class="vue-mzc-loading__spiner"
      :style="`width: ${size}; height: ${size};`"
    >
      <div
        v-for="(item, i) in [1, 2, 3, 4]"
        :key="i"
        :style="`
          width: ${size}; 
          height: ${size}; 
          border-width: ${width}; 
          border-color: ${color} transparent transparent transparent;`"
      ></div>
    </div>
    <div
      v-if="title"
      class="vue-mzc-loading__title"
      :style="`color: ${color};`"
    >
      {{ title }}
    </div>
  </div>
</template>

<style scoped>
.vue-mzc-loading {
  display: flex;
  align-items: center;
}
.vue-mzc-loading__spiner {
  display: block;
  position: relative;
}
.vue-mzc-loading__spiner div {
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  border-style: solid;
  border-radius: 50%;
  animation: vue-mzc-loading 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
  box-sizing: border-box;
}
.vue-mzc-loading__spiner div:nth-child(1) {
  animation-delay: -0.45s;
}
.vue-mzc-loading__spiner div:nth-child(2) {
  animation-delay: -0.3s;
}
.vue-mzc-loading__spiner div:nth-child(3) {
  animation-delay: -0.15s;
}
.vue-mzc-loading__title {
  padding-left: 8px;
  color: #000;
}
@keyframes vue-mzc-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>
