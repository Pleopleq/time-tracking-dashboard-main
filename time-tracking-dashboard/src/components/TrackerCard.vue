<template>
  <div class="tracker__container" :class="getColorBar(colorBar)">
    <div class="tracker__data">
      <slot name="trackerData"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    colorBar: {
      type: String,
      default: "",
    },
  },
  methods: {
    getColorBar(trackerName) {
      switch (trackerName) {
        case "work":
          return "colorBar__work";
        case "play":
          return "colorBar__play";
        case "study":
          return "colorBar__study";
        case "exercise":
          return "colorBar__exercise";
        case "social":
          return "colorBar__social";
        case "self care":
          return "colorBar__selfCare";
        default:
          return "";
      }
    },
  },
};
</script>

<style>
.tracker__container {
  display: flex;
  align-items: flex-end;
  border-radius: 15px;
  height: 130px;
  margin-bottom: 2rem;
}

.tracker__data {
  width: 280px;
  height: 100px;
  max-width: 320px;
  background-color: var(--dark-blue);
  border-radius: 12px;
}

.colorBar__work {
  background-color: var(--light-red);
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
