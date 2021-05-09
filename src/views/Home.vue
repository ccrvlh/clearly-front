<template>
  <div class="home">
    <el-row>
        <el-col :span="6">
          <WorkersCard />
        </el-col>
        <el-col :span="6">
          <WorkersCard />
        </el-col>
        <el-col :span="6">
          <WorkersCard />
        </el-col>
        <el-col :span="6">
          <WorkersCard />
        </el-col>
    </el-row>
    <el-row>
      <el-col :span="12">
        <StaticTaskChart/>
      </el-col>
      <el-col :span="12">
        <StaticTaskChart/>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import WorkersCard from '@/components/WorkersCard.vue'
import StaticTaskChart from '@/components/StaticTaskChart.vue'

export default {
  name: 'Home',
  components: {
    WorkersCard,
    StaticTaskChart
  }
}
</script>

<style scoped>


</style>