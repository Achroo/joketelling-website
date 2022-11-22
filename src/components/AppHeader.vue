<template>
  <h1 class="header">{{ text }}</h1>
</template>

<script>
export default {
  props: ["text"]
};
console.log("Loaded header");
</script>

<style>
.header {
  font-size: 2rem;
  text-align: center;
  padding-top: 2.75rem;
}
</style>
