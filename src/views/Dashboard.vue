<template>
  <div class="home">
    <el-row :gutter="20">
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
    <br>
    <el-row :gutter="20">
      <el-col :span="12">
        <PieChart/>
      </el-col>
      <el-col :span="12">
        <LineChart/>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import WorkersCard from '@/components/WorkersCard.vue'
import PieChart from '@/components/PieChart.vue'
import LineChart from '@/components/LineChart.vue'

export default {
  name: 'Home',
  components: {
    WorkersCard,
    PieChart,
    LineChart
  }
}
</script>

<style scoped>


</style>