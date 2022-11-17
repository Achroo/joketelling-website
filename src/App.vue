<template>
  <div id="appContainer">
    <AppHeader text="Tell me a joke app" />
    <JokeButton text="Tell me a joke" />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import JokeButton from "./components/JokeButton.vue";

export default {
  name: "App",
  components: {
    AppHeader: AppHeader,
    JokeButton: JokeButton,
  },
};
</script>

<style>
#appContainer {
  margin: 0 auto;
  width: 60%;
  height: 350px;
  background-color: #abdbe3;
  border-radius: 5%;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}
</style>
