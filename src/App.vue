<template>
  <div id="app">
    <img src="./assets/giphy.gif" />
    <h1>insoo's Draggable</h1>
    <div class="helo"><HelloWorld /></div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #574b90;
  color: aliceblue;
}
.helo {
  display: flex;
  justify-content: center;
}
</style>
