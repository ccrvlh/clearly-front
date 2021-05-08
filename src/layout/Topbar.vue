<template>
  <div class="topnav">
      <ul>
        <el-button @click="$router.push('/')">CLEARLY</el-button>
        <el-button @click="$router.push('/')">Home</el-button>
        <el-button @click="$router.push('tasks')">Tasks</el-button>
        <el-button @click="$router.push('workers')">Workers</el-button>
        <el-button @click="$router.push('brokers')">Brokers</el-button>
      </ul>
  </div>
</template>

<script>
export default {
    name: 'Topbar'
}
</script>

<style scoped>

.topnav {
  text-align: center;
  background-color: rgb(16, 17, 26);
  overflow: hidden;
}

ul {
  display: inline;
  padding-top: 15px;
  padding-bottom: 15px;
  margin-left: 5%;
  color: grey;
  float: left;
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