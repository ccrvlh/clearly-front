<template>
    <div class='all__content'>
      <div class="all__information">
        <slot> </slot>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Content'
}
</script>

<style scoped>

.all__content {
  background: rgb(240, 241, 244);
  border-top: grey;
  border-width: 1px;
  width: 100%;
  height: 100%;
  display: flex;
  flex-flow: column;
  position: fixed;
}

.all__information {
  width: 90%;
  height: 95%;
  border:grey;
  border-width: 10px;
  /* background: white; */
  position:relative;
  margin:auto;
  box-shadow: grey;
}

</style>