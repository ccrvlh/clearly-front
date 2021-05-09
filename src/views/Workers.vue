<template>
  <div class="tasks">
    <div>
        <el-card>
            <el-row align="middle">
                <el-col :span="3">Name</el-col>
                <el-col :span="3">Status</el-col>
                <el-col :span="3">Concurrency</el-col>
                <el-col :span="3">Successful</el-col>
                <el-col :span="3">Failed</el-col>
                <el-col :span="2">Running</el-col>
                <el-col :span="2">Ratio</el-col>
                <el-col :span="3">Queues</el-col>
                <el-col :span="2">Action</el-col>
            </el-row>
        </el-card>
    </div>
    <br>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
    <div style="margin-bottom: 10px"><WorkerRow /></div>
  </div>
</template>

<script>
import WorkerRow from '@/components/WorkerRow'

export default {
  components: {WorkerRow}
}
</script>

<style scoped>



</style>