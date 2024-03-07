<template>
  <div>
    <nav>
      <ul class="nav-list">
        <li class="nav-item" v-for="(icon, index) in iconUrl" :key="index">
          <img :src="icon" alt="#" />
        </li>
      </ul>
      <div class="nav-plus">
        <div class="wrapper">
          <span class="plus-icon"></span>
        </div>
      </div>
    </nav>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      iconUrl: [
        require("../assets/nav/logo-horisontal.png"),
        require("../assets/nav/tools.png"),
        require("../assets/nav/build.png"),
        require("../assets/nav/money.png"),
        require("../assets/nav/data.png"),
        require("../assets/nav/doc.png"),
        require("../assets/nav/snow-icon.png"),
        require("../assets/nav/settings.png"),
        require("../assets/nav/chart.png"),
        require("../assets/nav/profiles.png"),
      ],
    };
  },
});
</script>

<style scoped>
nav {
  padding: 28px 0 0 0;
  width: 72px;
  box-sizing: border-box;
  height: 100vh;
  position: absolute;
  left: 0;
  top: 0;
  background-color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-self: center;
  border-radius: 10px 0 0 10px;
}

.nav-item {
  display: flex;
  align-items: center;
  list-style: none;
  margin-bottom: 20px;
  justify-content: center;
}

.nav-list {
  border-bottom: 1px solid #ddd;
  height: 100%;
}

.nav-item:first-child {
  margin-bottom: 28px;
}

.nav-item img {
  width: 20px;
  height: 20px;
}

.nav-plus {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 20px;
  height: 20px;
  padding: 26px;
}

.wrapper {
  width: 20px;
  height: 20px;
  background-color: #7d5fff;
  border-radius: 5px;
  position: relative;
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
