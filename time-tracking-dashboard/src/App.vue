<template>
  <main class="main__container">
    <user-profile @option-active="handleTimeframes">
      <template v-slot:avatar>
        <user-avatar></user-avatar>
      </template>
      <template v-slot:info>
        <user-info></user-info>
      </template>
    </user-profile>
    <div class="trackers__container">
      <tracker-card
        v-for="area in trackers"
        :key="area.title"
        :colorBar="area.title.toLowerCase()"
      >
        <template v-slot:trackerData>
          <tracker-data
            :title="area.title"
            :timeframe="area.timeframes[timeframe]"
          ></tracker-data>
        </template>
      </tracker-card>
    </div>
  </main>
</template>

<script>
import UserAvatar from "./components/UserAvatar.vue";
import UserInfo from "./components/UserInfo.vue";
import UserProfile from "./components/UserProfile.vue";
import TrackerCard from "./components/TrackerCard.vue";
import TrackerData from "./components/TrackerData.vue";
import data from "../public/data.json";

export default {
  name: "App",
  components: { UserProfile, UserAvatar, UserInfo, TrackerCard, TrackerData },
  data() {
    return {
      trackers: data,
      timeframe: "weekly",
    };
  },
  methods: {
    handleTimeframes(timeframe) {
      this.timeframe = timeframe;
    },
  },
};
</script>

<style>
@import "./assets/styles/styles.css";

.main__container {
  display: grid;
  grid-column: 320px;
  margin-top: 3.5rem;
  justify-content: center;
  align-content: center;
}
.trackers__container {
  margin-top: 1.5rem;
}
</style>
