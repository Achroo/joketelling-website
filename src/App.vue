<template>
  <div id="appContainer">
    <AppHeader text="Tell me a joke app" />
    <img src="./assets/laugh.png" class="laugh" />
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
    JokeButton: JokeButton
  }
};
</script>

<style>
.laugh {
  display: flex;
  justify-items: center;
  margin: 0 auto;
  padding-top: 2rem;
  padding-bottom: 2rem;
}

#appContainer {
  margin: 0 auto;
  width: 50%;
  padding-bottom: 2rem;
  background-color: #3498db;
  border-radius: 5px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}

@media only screen and (max-width: 600px) {
  #appContainer {
    width: 85%;
  }
}
</style>
