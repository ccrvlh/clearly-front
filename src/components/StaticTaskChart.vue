<template>
  <div>
    <el-card>
      <charts :options="chartOptions"/>
    </el-card>
  </div>
</template>

<script>
export default {
    name: 'StaticTaskChart',
    data() {
      return {
        chartOptions: {
          series: [{
              stack: 'normal',
              type: 'column',
              color: 'dark-blue',
              data: [1,2,3,6,2,3,4,1,6,7,6,5,4,3,2,1,2,3,4,5,6]
            },{
              stack: 'normal',
              type: 'column',
              color: 'red',
              data: [0,0,0,2,1,0,0,0,1,0,0,0,2,0,3,0,1,1,0,0,0]
            }],
        plotOptions: {
          column: {
            stacking: 'normal',
            lineColor: '#666666',
            lineWidth: 1,
            marker: {
              lineWidth: 1,
              lineColor: '#666666'
            }
          }
        },            
        }
      }
    }    
}
</script>

<style>

</style>