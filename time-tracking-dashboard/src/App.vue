<template>
  <main class="main__container">
    <user-profile>
      <template v-slot:avatar>
        <user-avatar></user-avatar>
      </template>
      <template v-slot:info>
        <user-info></user-info>
      </template>
    </user-profile>
  </main>
</template>

<script>
import UserAvatar from "./components/UserAvatar.vue";
import UserInfo from "./components/UserInfo.vue";
import UserProfile from "./components/UserProfile.vue";
export default {
  components: { UserProfile, UserAvatar, UserInfo },
  name: "App",
};
</script>

<style>
@import "./assets/styles/styles.css";

.main__container {
  display: grid;
  grid-column: 320px;
  justify-content: center;
  align-content: center;
}
</style>
