<template>
  <section class="container">
    <h2>{{ user.userName }}</h2>
    <button @click="addAge">Add 1 to Age</button>
    <h3>Age: {{ user.age }}</h3>
  </section>
</template>

<script setup>
import {reactive} from 'vue';


const user = reactive({
  userName: 'Maximilian',
  age: 5,
});

function addAge() {
  user.age ++;
}

</script>

<style>
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

.container {
  margin: 3rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  padding: 1rem;
  text-align: center;
}
</style>