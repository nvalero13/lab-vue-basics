<template>
  <header>
    <h2>Iteration 1: Navbar</h2>
    <li>  
      <ul><a href="#">Page 1</a></ul>
      <ul><a href="#">Page 2</a></ul>
      <ul><a href="#">Page 3</a></ul>
    </li>
  </header>
</template>

<script>
export default {};
</script>

<style scoped>
header {
  height: 100px;
  width: 100%;
  background-color: rgb(232, 83, 70);
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 10px;
}

li {
  display: flex;
  gap: 10px
}

a {
  text-decoration: none;
  color: white;
}

h2 {
  color: white;
}
</style>