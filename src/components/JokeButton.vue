<template>
  <button class="jokeButton" v-on:click="joke">{{ text }}</button>
</template>

<script>
import Artyom from "artyom.js";
const artyom = new Artyom();

artyom.fatality();

artyom
  .initialize({
    lang: "en-GB", // A lot of languages are supported. Read the docs !
    continuous: true, // Artyom will listen forever
    listen: false, // Start recognizing
    debug: true, // Show everything in the console
    speed: 1 // talk normally
  })
  .then(function() {
    console.log("Ready to work !");
  });

const JOKES = [
  "Knock, knock. Whos there? very long pause…. Java.",
  "Programming is like sex: One mistake and you have to support it for the rest of your life.",
  "The computer is mightier than the pen, the sword, and usually, the programmer.",
  "Programmer: A machine that turns coffee into code",
  "A SQL query goes into a bar, walks up to two tables and asks, Can I join you?",
  "The C language combines all the power of assembly language with all the ease-of-use of assembly language.",
  "Why do Java programmers have to wear glasses? Because they dont C#."
];

function joke() {
  let joke = JOKES[Math.floor(Math.random() * JOKES.length)];
  console.log(joke);
  artyom.say(joke);
}

export default {
  props: ["text"],
  methods: {
    joke: joke
  }
};
</script>

<style>
.jokeButton {
  margin: 0 auto;
  width: 200px;
  height: 50px;
  background-color: #e67e22;
  font-size: 1.1rem;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  border: none;
  border-radius: 5px;
}

.jokeButton:hover {
  background-color: #f39c12;
  cursor: pointer;
}
</style>
