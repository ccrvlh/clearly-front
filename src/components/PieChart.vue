Gr<template>
  <div>
    <el-card>
      <charts :options="chartOptions"/>
    </el-card>
  </div>
</template>

<script>
export default {
    name: 'PieChart',
    data() {
      return {
        chartOptions: {

    chart: {
        plotBackgroundColor: null,
        plotBorderWidth: null,
        plotShadow: false,
        type: 'pie'
    },
    title: {
        text: 'Celery Tasks'
    },
    tooltip: {
        pointFormat: '{series.name}: <b>{point.percentage:.1f}%</b>'
    },
    accessibility: {
        point: {
            valueSuffix: '%'
        }
    },
    plotOptions: {
        pie: {
            allowPointSelect: true,
            cursor: 'pointer',
            innerSize: '70%',
            dataLabels: {
                enabled: true,
                format: '<b>{point.name}</b>: {point.percentage:.1f} %'
            }
        }
    },
    series: [{
        name: 'Brands',
        colorByPoint: true,
        data: [{
            name: 'Success',
            y: 61.41,
            sliced: true,
            color: "rgb(165, 211, 138)"
        }, {
          name: 'Processing',
            y: 11.84,
            selected: true,
            color: 'rgb(199, 199, 199)'
        }, {
          name: 'Failed',
            y: 11.84,
            selected: true,
            color: 'rgb(240, 120, 120)'
        }]
    }]
  
        }
      }
    }    
}
</script>

<style>


</style>