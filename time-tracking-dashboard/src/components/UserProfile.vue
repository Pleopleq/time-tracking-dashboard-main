<template>
  <div class="userProfile">
    <div class="userProfile__container">
      <slot name="avatar"></slot>
      <slot name="info"></slot>
    </div>
    <div class="userProfile__timelines">
      <button>Daily</button>
      <button>Weekly</button>
      <button>Monthly</button>
    </div>
  </div>
</template>
<script>
export default {};
</script>

<style>
.userProfile {
  background-color: var(--dark-blue);
  border-radius: 12px;
}
.userProfile__container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 280px;
  height: 120px;
  max-width: 320px;
  background-color: var(--blue);
  border-radius: 12px;
}

.userProfile__timelines {
  display: flex;
  justify-content: space-around;
  background-color: var(--dark-blue);
  border-radius: 12px;
}

.userProfile__timelines > button {
  background-color: transparent;
  font-family: inherit;
  font-weight: 400;
  color: white;
  border: none;
  padding: 1.2rem;
}
</style>
