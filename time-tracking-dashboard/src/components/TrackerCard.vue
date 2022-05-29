<template>
  <div class="tracker__container">
    <div class="tracker__colorBar"></div>
    <div class="tracker__data"></div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.tracker__data {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 280px;
  height: 120px;
  max-width: 320px;
  background-color: var(--dark-blue);
  border-radius: 12px;
}
</style>
