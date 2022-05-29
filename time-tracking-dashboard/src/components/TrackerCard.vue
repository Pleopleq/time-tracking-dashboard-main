<template>
  <div class="tracker__container" :class="colorBar">
    <div class="tracker__data">
      <slot name="trackerData"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    colorBar: "",
  },
};
</script>

<style>
.tracker__container {
  display: flex;
  align-items: flex-end;
  border-radius: 15px;
  height: 130px;
}
.tracker__data {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 280px;
  height: 100px;
  max-width: 320px;
  background-color: var(--dark-blue);
  border-radius: 12px;
}

.colorBar__work {
  background-color: var(--soft-orange);
}
.colorBar__play {
  background-color: var(--soft-blue);
}
.colorBar__study {
  background-color: var(--light-red-study);
}
.colorBar__exercise {
  background-color: var(--lime-green);
}
.colorBar__social {
  background-color: var(--violet);
}
.colorBar__selfCare {
  background-color: var(--soft-orange);
}
</style>
