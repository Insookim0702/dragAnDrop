<template>
  <div id="app">
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Ranchers&display=swap"
      rel="stylesheet"
    />
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
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #574b90;
  color: aliceblue;
  font-family: "Ranchers", cursive;
}
.helo {
  display: flex;
  justify-content: center;
}
</style>
