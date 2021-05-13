<template>
  <div id="app">
    <TwitterBoxClient />
  </div>
</template>

<script>
import TwitterBoxClient from "./components/TwitterBoxClient.vue";

export default {
  name: "App",
  components: {
    TwitterBoxClient,
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
  margin-top: 60px;
}
</style>
<style src="./assets/tailwind.css" />
