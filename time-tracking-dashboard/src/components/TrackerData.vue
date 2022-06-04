<template>
  <section class="trackerData">
    <div class="rightData__container">
      <h2>{{ title }}</h2>
      <h1>{{ timeframe.weekly.current }}</h1>
    </div>
    <div class="leftData__container">
      <div>...</div>
      <p>Last Week - {{ timeframe.weekly.previous }}</p>
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

<style></style>
