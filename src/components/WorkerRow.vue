<template>
  <div>
      <el-card>
          <el-row>
              <el-col :span="4"><el-tag>Live</el-tag></el-col>
              <el-col :span="4">celery@aws-423-fnj</el-col>
              <el-col :span="3">12.214</el-col>
              <el-col :span="3">126</el-col>
              <el-col :span="3">98,7%</el-col>
              <el-col :span="3">Node</el-col>
              <el-col :span="4"><el-button>View</el-button></el-col>
          </el-row>
      </el-card>
  </div>
</template>

<script>
export default {
    name: 'WorkerRow'
}
</script>

<style>

</style>