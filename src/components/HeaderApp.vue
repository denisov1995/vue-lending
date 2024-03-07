<template>
  <div>
    <header>
      <div class="header-tools">
        <div>
          <img src="../assets/burger.png" alt="#" class="burger-menu" />
          <p class="team">Team</p>
        </div>
        <div>
          <img src="../assets/main-search.png" alt="#" class="search" />
          <img src="../assets/notification.png" alt="#" class="notification" />
        </div>
      </div>
      <div class="profile">
        <img src="../assets/profile-photo.png" alt="" />
        <p class="profile-name">Ernest Eberly</p>
        <img src="../assets/dropdown-blue.png" alt="#" />
      </div>
    </header>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped>
header {
  display: flex;
  align-items: center;
  max-width: 100%;
  padding: 16px 0;
  background-color: #fff;
  border-radius: 0 10px 0 0 ;
  margin-left: 72px;
}

.header-tools {
  display: flex;
  justify-content: space-between;
  width: 100%;
  padding: 0 28px;
  border-right: 1px solid #ddd;
}

.header-tools div {
  display: flex;
  align-items: center;
}

.burger-menu {
  height: 11px;
  width: 16px;
  margin-right: 28px;
}

.team {
  font-size: 22px;
}

.search {
  margin-right: 28px;
}

.profile {
  display: flex;
   padding: 0 28px;
   align-items: center;
}

.profile img:first-child {
  margin-right: 12px;
}

.profile img:last-child {
  width: 20px;
  height: 20px;
}

.profile-name {
   white-space: nowrap;
   margin-right: 12px;
}
</style>
