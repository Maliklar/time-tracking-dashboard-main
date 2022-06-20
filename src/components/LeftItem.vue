<template>
  <div class="left-item">
    <div class="upper-card">
      <img src="../assets/image-jeremy.png" alt="avatar" class="avatar" />
      <div>
        <div class="report-for">Report for</div>
        <div class="user-name">Jeremy Robson</div>
      </div>
    </div>
    <div class="lower-card">
      <div class="option" :class="day" @click="toggleOption('day')">Daily</div>
      <div class="option" :class="week" @click="toggleOption('week')">
        Weekly
      </div>
      <div class="option" :class="month" @click="toggleOption('month')">
        Monthly
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      timeframe: "week",
      day: "",
      week: "active",
      month: "",
    };
  },
  methods: {
    toggleOption(option) {
      this.timeframe = option;
      this.$emit("timeframe", this.timeframe);
      if (option == "day") {
        this.day = "active";
        this.week = "";
        this.month = "";
      }
      if (option == "week") {
        this.week = "active";
        this.month = "";
        this.day = "";
      }
      if (option == "month") {
        this.month = "active";
        this.week = "";
        this.day = "";
      }
    },
  },
};
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

.option {
  color: var(--PaleBlue);
  cursor: pointer;
}
.option:hover {
  color: white;
}
.active {
  color: white;
}

@media screen and (max-width: 1050px) {
  .upper-card {
    background-color: var(--Blue);
    height: 68.5%;
    display: flex;
    flex-direction: row;
    text-align: start;
    align-items: center;
    justify-content: space-evenly;
    padding: 20px;
    box-sizing: border-box;
  }
  .lower-card {
    flex-grow: 1;
    display: flex;
    flex-direction: row;
    text-align: start;
    justify-content: space-evenly;
    margin: 30px 0px;
  }
  .report-for {
    margin-top: 0px;
    color: var(--PaleBlue);
  }

  .user-name {
    font-size: 22px;
    font-weight: 300;
    margin-top: 2px;
  }
}
</style>