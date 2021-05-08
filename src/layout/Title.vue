<template>
  <div class='title__bar'>
        <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
    name: 'Title',
    props: {
        title: String
    }
}
</script>

<style scoped>

.title__bar {
    box-shadow: 0 2px 4px rgba(0, 0, 0, .12), 0 0 6px rgba(0, 0, 0, .04);
    border-bottom: rgba(0, 0, 0, .04);
    background: white;
    padding: 20px;
    text-align: left;
    padding-left: 5%;
}


</style>