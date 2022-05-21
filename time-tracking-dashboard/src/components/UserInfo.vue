<template>
  <div class="userInfo">
    <p class="userInfo__report">{{ reportedFor }}</p>
    <h1 class="userInfo__username">{{ userName }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reportedFor: "Report for",
      userName: "Jeremy Robson",
    };
  },
};
</script>

<style></style>
