<template>
  <div class="left-item">
    <div class="upper-card">
      <img src="../assets/image-jeremy.png" alt="avatar" class="avatar" />
      <div class="report-for">Report for</div>
      <div class="user-name">Jeremy Robson</div>
    </div>
    <div class="lower-card">
      <div id="daily">Daily</div>
      <div id="weekly">Weekly</div>
      <div id="monthly">Monthly</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.left-item {
  grid-row: 1 / -1;
  background-color: var(--Darkblue);
  border-radius: 15px;
  color: white;

  display: flex;
  flex-direction: column;
}

.left-item > * {
  border-radius: 15px;
}
.upper-card {
  background-color: var(--Blue);
  height: 68.5%;
  display: flex;
  flex-direction: column;
  text-align: start;
  padding-top: 34px;
  padding-left: 27px;
  box-sizing: border-box;
}

.lower-card {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  text-align: start;
  justify-content: space-evenly;
  margin-left: 28px;
  margin-bottom: 8px;
  margin-top: 6px;
  font-size: 18px;
}

.avatar {
  border: solid 3px white;
  border-radius: 100%;
  height: 78px;
  width: 78px;
}

.user-name {
  font-size: 42px;
  font-weight: 300;
  margin-top: 2px;
}

.report-for {
  margin-top: 38px;
  color: var(--PaleBlue);
}

#daily {
  color: var(--PaleBlue);
}
#monthly {
  color: var(--PaleBlue);
}
</style>