<template>
  <button class="jokeButton" v-on:click="joke">{{ text }}</button>
</template>

<script>
function joke() {
  console.log("Joke");
}

export default {
  props: ["text"],
  methods: {
    joke: joke,
  },
};
</script>

<style>
.jokeButton {
  margin: 0 auto;
  width: 200px;
  height: 50px;
  background-color: blue;
  font-size: 1rem;
  color: white;
}
</style>