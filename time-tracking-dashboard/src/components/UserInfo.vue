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

<style>
.userInfo__report {
  margin: 0;
  font-weight: 300;
  font-size: 0.8em;
}

.userInfo__username {
  margin-top: 0.4rem;
  font-weight: 400;
}
</style>
