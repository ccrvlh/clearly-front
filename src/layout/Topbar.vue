<template>
  <div class="topnav">
        <span class="menu__left">

          <b style="margin-right: 40px; font-weight: 2000; color: white;">CLEARLY</b>

          <router-link to="/">
            <el-button>Home</el-button>
          </router-link>

          <router-link to="tasks">
            <el-button>Tasks</el-button>
          </router-link>

          <router-link to="workers">
            <el-button>Workers</el-button>
          </router-link>

          <router-link to="brokers">
            <el-button>Brokers</el-button>
          </router-link>
      
        </span>
        <span class="menu__right">

          <router-link to="settings">
            <el-button>Settings</el-button>
          </router-link>

          <el-button @click='openLink("https://www.github.com")'>Docs</el-button>
          <el-button @click='openLink("https://www.github.com")'>GitHub</el-button>
      
        </span>

  </div>
</template>

<script>
export default {
    name: 'Topbar',
    methods: {
      openLink(website) {
        window.open(website)
      }
    }
}
</script>

<style scoped>

.topnav {
  text-align: center;
  background-color: rgb(16, 17, 26);
  overflow: hidden;
}


.menu__left {
  display: inline;
  padding-top: 15px;
  padding-bottom: 15px;
  margin-left: 5%;
  color: grey;
  float: left;
  text-decoration: none;
}

.menu__right {
  display: inline;
  padding-top: 15px;
  padding-bottom: 15px;
  margin-right: 5%;
  color: grey;
  float: right;
  text-decoration: none;
}


.el-button {
  font-family: 'Open Sans';
  font-weight: bold;
  background-color: rgb(16, 17, 26);
  border: 0px
}

.el-button:hover {
  background-color: rgb(44, 45, 54);
  font-weight: bold;
  border: 0px;
  color: white;
}

.el-button:focus {
  font-weight: bold;
  background-color: rgb(44, 45, 54);
  border: 0px;
  color: white;
}

.el-button:active {
  font-weight: bold;
  background-color: rgb(16, 17, 26);
  border: 0px;
  color: white;
}

.el-button:visited {
  font-weight: bold;
  background-color: rgb(16, 17, 26);
  border: 0px;
  color: white;
}




</style>