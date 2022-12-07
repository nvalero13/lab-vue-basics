<template>
  <Navbar />
  <section>
    <h3>Iteration 2.1: <span>{{2+2}}</span></h3>
    <h3>Iteration 2.2: <span>{{getString()}}</span></h3>
<hr/>
<div class="it-container">
    <button @click="toggleVisibility"><h3>Iteration 3: Button</h3></button>
    <div v-show="visible" class="iteration3">
      <h3>Iteration 3: Cool element</h3>
    </div>
  </div>
  <hr/>
  <List />
  <hr>
  <div class="it-container">
    <button @click="changeBackground"><h3>Iteration 5: Button</h3></button>
    <div class="iteration3" :style="(bgColor)">
      <h3>Iteration 5: Cool element</h3>
    </div>
  </div>


  </section>

  <Footer />
</template>

<script setup>
import { ref } from "vue";

import List from "./components/List.vue";
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";

function getString() {
  return "This is a string returned by a function"
}

const visible = ref(false);

function toggleVisibility() {
  visible.value = !visible.value
}

const bgColor = ref("background-color: blue");

function changeBackground() {
  bgColor.value === "background-color: blue" ? bgColor.value = "background-color: green" : bgColor.value = "background-color: blue" ;
}

</script>

<style>
section {
  margin: 0 auto;
  max-width: 1200px;
  padding: 10px
}

h3 span {
  color: grey
}

.it-container {
  display: flex;
  gap: 10px;
  height:  70px;
}

.iteration3 {
  padding: 0 20px;
  width: 75%;
  color: white;
  background-color: rgb(232, 83, 70);
}

button {
  background-color: white;
  width: 20%;
  height: 100%;
  border: 1px solid rgb(232, 83, 70);
  
  color: rgb(232, 83, 70);
  cursor: pointer;
}

button:hover {
  background-color: rgb(232, 83, 70);
  color: white;
}

hr {
  box-shadow: none;
  border: none;
  height: 1px;
  background-color: rgb(232, 83, 70);
  margin: 20px 0;
}
</style>
