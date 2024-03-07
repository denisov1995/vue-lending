<template>
  <div id="app">
      <HeaderApp />
      <NavList />
      <div class="main">
        <TopBar :stats="stats" />
        <EmployeeTable :employees="employees" />
      </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import NavList from "./components/NavList.vue";
import HeaderApp from "./components/HeaderApp.vue";
import TopBar from "./components/TopBar.vue";
import EmployeeTable from "./components/EmployeeTable.vue";

export default Vue.extend({
  name: "App",
  components: {
    HeaderApp,
    NavList,
    TopBar,
    EmployeeTable,
  },
  data() {
    return {
      stats: [
        {
          name: "members",
          count: 130,
        },
        {
          name: "online",
          count: 36,
          online: true,
        },

        {
          name: "men",
          count: 50,
        },
        {
          name: "women",
          count: 80,
        },

        {
          name: "average age",
          count: 29,
        },
        {
          name: "days work on average",
          count: 36,
        },
        {
          name: "days work newest employee",
          count: 265,
        },
        {
          name: "days work oldest employee",
          count: 1256,
        },
      ] as IStat[],
      employees: [
        {
          businessName: "Sarah Connor",
          team: "Crosty",
          role: "Team Lead",
          gmail: "sarahconnor@gmail.com",
          birthday: "25.04.1994",
          telegram: "@sarahconnor",
          lastLogin: "03.11.2021",
          userPermissions: "Edit",
          photo: require("./assets/employee/sarah.png"),
        },
        {
          businessName: "Arnold Brown",
          team: "Gunters",
          role: "Seo Specialist",
          gmail: "arnoldbrown@gmail.com",
          birthday: "12.04.1989",
          telegram: "@arnoldbrown",
          lastLogin: "02.11.2021",
          userPermissions: "Edit",
          photo: require("./assets/employee/arnold.png"),
        },
        {
          businessName: "Ernest Eberly",
          team: "Flamethrower",
          role: "Semantic Specialist",
          gmail: "ernesteberly@gmail.com",
          birthday: "17.06.1993",
          telegram: "@ErnestEberly",
          lastLogin: "03.11.2021",
          userPermissions: "Edit",
          photo: require("./assets/employee/ernest.png"),
        },
        {
          businessName: "Lance Thomas",
          team: "Wizards",
          role: "Seo Specialist",
          gmail: "lancethomas@gmail.com",
          birthday: "12.04.1989",
          telegram: "@LanceThomas",
          lastLogin: "01.11.2021",
          userPermissions: "Edit",
          photo: require("./assets/employee/lanceT.png"),
        },
        // {
        //   businessName: "Cheryl Glover",
        //   team: "Gunters",
        //   role: "Python Programmist",
        //   gmail: "cherylglover@gmail.com",
        //   birthday: "15.08.1985",
        //   telegram: "@CherylGlover",
        //   lastLogin: "03.11.2021",
        //   userPermissions: "Edit",
        //   photo: require("./assets/employee/cheryl.png"),
        // },
        // {
        //   businessName: "Lance Thomas",
        //   team: "Crosty",
        //   role: "Seo Specialist",
        //   gmail: "lancethomas@gmail.com",
        //   birthday: "12.04.1989",
        //   telegram: "@LanceThomas",
        //   lastLogin: "01.11.2021",
        //   userPermissions: "Edit",
        //   photo: require("./assets/employee/lance.png"),
        // },
        // {
        //   businessName: "Ernest Eberly",
        //   team: "Flamethrower",
        //   role: "Semantic Specialist",
        //   gmail: "ernesteberly@gmail.com",
        //   birthday: "17.06.1993",
        //   telegram: "@ErnestEberly",
        //   lastLogin: "03.11.2021",
        //   userPermissions: "Edit",
        //   photo: require("./assets/employee/ernest.png"),
        // },
        // {
        //   businessName: "Lance Thomas",
        //   team: "Wizards",
        //   role: "Seo Specialist",
        //   gmail: "lancethomas@gmail.com",
        //   birthday: "12.04.1989",
        //   telegram: "@LanceThomas",
        //   lastLogin: "01.11.2021",
        //   userPermissions: "Edit",
        //   photo: require("./assets/employee/lanceT.png"),
        // },
        // {
        //   businessName: "Cheryl Glover",
        //   team: "Gunters",
        //   role: "Python Programmist",
        //   gmail: "cherylglover@gmail.com",
        //   birthday: "15.08.1985",
        //   telegram: "@CherylGlover",
        //   lastLogin: "03.11.2021",
        //   userPermissions: "Edit",
        //   photo: require("./assets/employee/cheryl.png"),
        // },
      ],
    };
  },
});

export interface IStat {
  name: string;
  count: number;
  online?: boolean;
}
</script>

<style>
body {
  width: 100%;
  height: 100vh;
  background-color: #e5e8ef;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  height: 100vh;
  display: flex;
  flex-direction: column;
}
* {
  margin: 0;
  padding: 0;
}

.main {
  padding: 28px;
  box-sizing: border-box;
  margin-left: 72px;
  position: relative;
  flex-grow: 1;
}
</style>
