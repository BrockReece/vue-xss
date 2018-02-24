<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
    <div v-html="test"></div>
  </div>
</template>

<script>
import xss from "./xss";
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data() {
    return {
      fields: ["name"],
      testData: [{ name: "test" }],
      test: xss
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
