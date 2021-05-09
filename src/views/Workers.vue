<template>
  <div class="tasks">
    <div>
        <el-card>
            <el-row>
                <el-col :span="4">Status</el-col>
                <el-col :span="4">Name</el-col>
                <el-col :span="3">Successful</el-col>
                <el-col :span="3">Failed</el-col>
                <el-col :span="3">Ratio</el-col>
                <el-col :span="3">Ratio</el-col>
                <el-col :span="4">Action</el-col>
            </el-row>
        </el-card>
    </div>    
    <WorkerRow />
    <WorkerRow />
    <WorkerRow />
    <WorkerRow />
    <WorkerRow />
    <WorkerRow />
    <WorkerRow />
    <WorkerRow />
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