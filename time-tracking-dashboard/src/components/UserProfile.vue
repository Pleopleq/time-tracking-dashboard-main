<template>
  <div class="userProfile__container">
    <slot name="avatar"></slot>
    <slot name="info"></slot>
  </div>
</template>
<script>
export default {};
</script>

<style>
.userProfile__container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 3.5rem;
  width: 280px;
  height: 120px;
  max-width: 320px;
  background-color: var(--blue);
  border-radius: 12px;
}
</style>
