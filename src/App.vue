<template>
  <div id="app">
    <Topbar />
    <Title :title="currentRouteName" />
    <Content>
      <router-view/>
    </Content>    
  </div>
</template>


<script>
import Topbar from './layout/Topbar.vue'
import Title from './layout/Title.vue'
import Content from './layout/Content.vue'

export default {
  components: {
    Topbar,
    Title,
    Content
  },
  computed: {
      currentRouteName() {
          return this.$route.name;
      }
  }
}

</script>



<style>
*,
*::after,
*::before {
box-sizing: border-box;
margin: 0;
padding: 0;
position: relative;
}


#app {
  font-family: 'Open Sans', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
