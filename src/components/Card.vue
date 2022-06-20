<template>
  <div class="card">
    <LeftItem />
    <Items :image="'icon-work.svg'" />
    <Items :image="'icon-work.svg'" />
    <Items :image="'icon-work.svg'" />
    <Items :image="'icon-work.svg'" />
    <Items :image="'icon-work.svg'" />
    <Items :image="'icon-work.svg'" />
  </div>
</template>

<script>
import Items from "./Items.vue";
import LeftItem from "./LeftItem.vue";
export default {
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
</style>