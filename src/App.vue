<template>
  <main>
    <Card :data="data" />
  </main>
</template>

<script>
import Card from "./components/Card.vue";
import object from "./assets/data.json";
export default {
  name: "App",
  components: { Card },

  data() {
    return {
      data: null,
    };
  },
  methods: {},
  async created() {
    this.data = object;
  },
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
