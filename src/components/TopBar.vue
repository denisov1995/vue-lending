<template>
  <div>
    <div class="topbar">
      <img src="../assets/team.png" class="team-ico" alt="#" />
      <div class="team-info">
        Team
        <img src="../assets/info.png" alt="#" />
      </div>
      <div class="team-stats">
        <div class="team-stat" v-for="stat in stats" :key="stat.label">
          <p class="count">{{ stat.count }}</p>
          <p class="subtitle">{{ stat.name }}</p>
        </div>
      </div>
    </div>
    <button class="team-button">
      <div class="wrapper">
        <span class="plus-icon"></span>
      </div>
      Add new Employee
    </button>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  props: {
    stats: Array,
  },
});
</script>

<style scoped>
.topbar {
  display: flex;
  align-items: center;
  margin-bottom: 28px;
  padding: 16px 28px;
  width: 70%;
  background-color: #fff;
  border-radius: 10px;
  width: fit-content;
}

.team-stats {
  display: flex;
}

.team-stat {
  padding: 0 36px;
  border-right: 1px solid #e5e8ef;
}

.team-stat:last-child {
  padding: 0 0 0 36px;
  border-right: none;
}

.team-ico {
  margin-right: 16px;
}

.team-info {
  font-size: 20px;
  margin-right: 72px;
  position: relative;
}

.team-info img {
  position: absolute;
  right: -20px;
}

.count {
  font-size: 22px;
  font-weight: bold;
  text-align: left;
  margin-bottom: 10px;
}

.subtitle {
  font-size: 12px;
  color: #8591ae;
}

.team-button {
  background-color: #8f20ef;
  color: white;
  border: none;
  border-radius: 15px;
  padding: 10px 20px;
  font-size: 16px;
  display: flex;
  align-items: center;
  cursor: pointer;
  transition: background-color 0.3s ease;
  padding: 16px;
  margin-bottom: 28px;
}

.team-button:hover {
  background-color: #6a3eab;
}

.wrapper {
  width: 20px;
  height: 20px;
  background-color: #7d5fff;
  border-radius: 5px;
  position: relative;
  margin-right: 10px;
}

.plus-icon::before,
.plus-icon::after {
  content: "";
  position: absolute;
  background-color: white;
  border-radius: 1px;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

.plus-icon::before {
  width: 10px;
  height: 2px;
}

.plus-icon::after {
  width: 2px;
  height: 10px;
}
</style>
