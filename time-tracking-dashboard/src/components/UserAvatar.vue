<template>
  <div class="userAvatar__container">
    <img
      class="userAvatar__avatar"
      src="../assets/images/image-jeremy.png"
      alt="user profile picture"
    />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
img {
  width: 100%;
  min-width: 32px;
  max-width: 62px;
  border: 2px solid white;
  border-radius: 100%;
}

.userAvatar__container {
  margin-right: 1rem;
}
</style>
