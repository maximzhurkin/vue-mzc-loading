<script>
import Vue from "vue";
import VueMzcLoading from "@/vue-mzc-loading.vue";

export default Vue.extend({
  name: "ServeDev",
  components: {
    VueMzcLoading,
  },
});
</script>

<template>
  <div id="app">
    <div class="row">
      <vue-mzc-loading />
    </div>
    <div class="row">
      <vue-mzc-loading title="Loading..." />
    </div>
    <div class="row">
      <vue-mzc-loading
        size="48px"
        width="8px"
        color="#539bf5"
        title="Custom loading..."
      />
    </div>
  </div>
</template>

<style>
  html,
  body,
  #app {
    height: 100%;
  }
  #app {
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
    justify-content: center;
    color: #ffffff;
    background-color: #22272e;
  }
  .row:not(:last-child) {
    margin-bottom: 32px;
  }
</style>