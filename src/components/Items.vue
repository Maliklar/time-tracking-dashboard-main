<template>
  <div class="item">
    <div class="header">
      <img :src="require('../assets/' + image)" alt="" />
    </div>
    <div class="body">
      <div class="body-controller">
        <div>Work</div>
        <img src="../assets/icon-ellipsis.svg" alt="" />
      </div>
      <div class="body-content">
        <div class="time">32hrs</div>
        <div class="description">Last Week - 36hrs</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
  },

  created() {
    console.log(this.image);
  },
};
</script>

<style scoped>
.item {
  background-color: var(--Darkblue);
  border-radius: 10px;
  color: white;
  display: flex;
  flex-direction: column;

  /* grid-template-columns: 1fr; */
}

.item > * {
  border-radius: 10px;
}
.header {
  background-color: var(--work);
  display: flex;
  flex-direction: row-reverse;
  overflow: hidden;
}
.header > img {
  margin-top: -10px;
  margin-right: 17px;
}

.body {
  background-color: var(--Darkblue);
  height: auto;
  flex-grow: 1;
  margin-top: -10%;
  display: flex;
  flex-direction: column;
}

.body-controller {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0px 30px;
  margin-top: 30px;
  box-sizing: border-box;
  font-size: 18px;
}
.body-content {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  text-align: start;
  gap: 10px;
  margin: 24px 30px;
}

.description {
  color: var(--PaleBlue);
  font-weight: 300;
  font-size: 14px;
  letter-spacing: 1px;
}

.time {
  font-size: 54px;
  font-weight: 300;
  letter-spacing: 0px;
}
</style>