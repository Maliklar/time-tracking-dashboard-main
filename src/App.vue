<template>
  <main>
    <Card />
  </main>
</template>

<script>
import Card from "./components/Card.vue";
export default {
  name: "App",
  components: { Card },
};
</script>

<style>
#app {
  background-color: var(--Verydarkblue);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0px;
}

body {
  margin: 0px;
  padding: 0px;
}
main {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  justify-items: center;
}
</style>
