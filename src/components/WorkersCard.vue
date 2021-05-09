<template>
  <div>
      <el-card>
          <div class="card__title">
            <p>
                WORKERS
            </p>
          </div>
          <br>
          <div class="card__number">
              <h1>23</h1> online
              <h1>3</h1> offline
          </div>
      </el-card>
  </div>
</template>

<script>
export default {
    name: 'WorkersCard'
}
</script>

<style>
.el-card {
    padding-bottom: 15px;
}
.card__title {
    float: left;
    color: gray;
    text-align: left;
    font-size: small;
}

</style>