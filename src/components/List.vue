<template>
  <h3>Iteration 4: List Rendering</h3>
  <div v-for="post in data" :key="post.title">
    <article>
      <h2>{{ post.title }}</h2>
      <h4>{{ post.description }}</h4>
      <p>{{ post.content }}</p>
    </article>
  </div>
</template>

<script setup>
import { ref } from "vue";

const data = ref([
  {
    title: "How to do something",
    description: "If you need help on how to do something this is your post",
    content:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus bibendum ullamcorper commodo. Cras porttitor ante nec lorem sollicitudin imperdiet.",
  },
  {
    title: "Look at what people do",
    description: "If you can't do anything what others do",
    content:
      "Nam aliquam blandit tempor. Ut ut eleifend justo, vel iaculis diam. Mauris ultricies auctor nulla, a suscipit eros varius nec.",
  },
  {
    title: "Are you a donut?",
    description: "Maybe you are a donut",
    content:
      "Maecenas volutpat aliquet sem id ultricies. Phasellus pharetra est ante, blandit mollis nunc blandit dapibus.",
  },
]);
</script>

<style scoped>
article {
  margin: 10px;
  padding: 10px 20px;
  border: 1px solid rgb(232, 83, 70);
}

h2 {
  color: rgb(232, 83, 70);
}
</style>
