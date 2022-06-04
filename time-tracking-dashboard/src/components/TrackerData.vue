<template>
  <section class="trackerData">
    <div class="rightData__container">
      <h2 class="title">{{ title }}</h2>
      <h1 class="currentHours">{{ timeframe.current }} hrs</h1>
    </div>
    <div class="leftData__container">
      <button class="moreDetails">
        <div>...</div>
      </button>
      <p class="lastWeekHours">Last Week - {{ timeframe.previous }}hrs</p>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    title: String,
    timeframe: Object,
  },
};
</script>

<style>
.trackerData {
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  align-items: center;
  height: 100%;
  margin: 0 22px;
}

.rightData__container {
  text-align: left;
}

.leftData__container {
  text-align: right;
}

.title {
  margin-bottom: 6px;
}

.moreDetails {
  background-color: transparent;
  color: white;
  border: none;
  font-size: 1.7em;
  margin-bottom: 12px;
}

.lastWeekHours {
  font-weight: 200;
  font-size: 0.8em;
  opacity: 0.8;
}
.currentHours {
  margin: 0;
  font-weight: 300;
  font-size: 1.5em;
}
</style>
