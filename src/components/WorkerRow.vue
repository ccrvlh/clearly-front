<template>
  <div>
      <el-card shadow="hover">
          <el-row>
              <el-col :span="3"><div style="vertical-align: baseline;">celery@aws-423-fnj</div></el-col>
              <el-col :span="3"><div style="vertical-align: baseline;"><el-tag>Live</el-tag></div></el-col>
              <el-col :span="3"><div style="vertical-align: baseline;">2</div></el-col>
              <el-col :span="3"><div style="vertical-align: baseline;">12.214</div></el-col>
              <el-col :span="3"><div style="vertical-align: baseline;">126</div></el-col>
              <el-col :span="2"><div style="vertical-align: baseline;">4</div></el-col>
              <el-col :span="2"><div style="vertical-align: baseline;">98,7%</div></el-col>
              <el-col :span="3"><div style="vertical-align: baseline;">read, process</div></el-col>
              <el-col :span="2"><div style="vertical-align: baseline;"><el-button>View</el-button></div></el-col>
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