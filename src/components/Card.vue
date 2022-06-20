<template>
  <div class="card">
    <LeftItem @timeframe="timeframe" />
    <template v-for="object in data" :key="object">
      <Items :object="object" :timeframe="time" />
    </template>
  </div>
</template>

<script>
import Items from "./Items.vue";
import LeftItem from "./LeftItem.vue";
export default {
  props: {
    data: Object,
  },
  data() {
    return {
      time: "week",
    };
  },
  methods: {
    timeframe(val) {
      this.time = val;
    },
  },
  components: { Items, LeftItem },
};
</script>

<style>
.card {
  margin: 0% 170px;
  padding: 0px;
  width: auto;
  min-height: 514px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(2, 1fr);

  grid-gap: 30px;
}

.test-item {
  background-color: blue;
}
.test-item:first-child {
  grid-row: 1 / -1;
}

@media screen and (max-width: 1050px) {
  .card {
    display: flex;
    flex-direction: column;
    margin: 10% 5%;
  }
}
</style>