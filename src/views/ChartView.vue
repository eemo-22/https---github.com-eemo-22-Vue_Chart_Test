<template>
  <h1>This is a Chart Example</h1>
  <BarChart 
    :chart-data="barChart01.chartData" 
    :chart-option="barChart01.chartOptions"
    :width="200" 
    :height="200"
    :chartId="'뭐임'"
  />
  <BarChart 
    :chart-data="barChart02.chartData" 
    :chart-option="barChart02.chartOptions" 
    :width="300" 
    :height="150"
    :chartId="'대체'"
  />
  <BarChart
    :chart-data="barChart03.chartData"
    :chart-option="barChart03.chartOptions"
    :width="300" 
    :height="150"
    :chartId="'진짜'"
  />
  <LineChart 
  :chart-data="barChart03.chartData"
    :chart-option="barChart03.chartOptions"
    :width="300" 
    :height="150"
    :chartId="'헤헤'"
  />
</template>

<script>
import BarChart from '../components/charts/BarChart.vue';
import LineChart from '../components/charts/LineChart.vue';
export default {
  components: {
    BarChart,
    LineChart
  },
  data() {
    return {
      barChart01: {
        chartData: {
          labels: [ '1월', '2월', '3월' ],
          datasets: [ 
            { 
              label: '월별',
              data: [40, 20, 12],
              backgroundColor: '#f87979',
            } 
          ] 
        },
        chartOptions: {
          responsive: true
        },
      },
      barChart02: {
        chartData: {
          labels: [ '어제', '오늘', '내일' ],
          datasets: [ 
            { 
              label: '날짜별',
              data: [70, 25, 50],
            }
          ] 
        },
        chartOptions: {
          responsive: true
        },
      },
      barChart03: {
        chartData: {
          labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
          datasets: [ 
            { 
              label: '# of Votes',
              data: [12, 19, 3, 5, 2, 3],
              backgroundColor: [
                  'rgba(255, 99, 132, 0.2)',
                  'rgba(54, 162, 235, 0.2)',
                  'rgba(255, 206, 86, 0.2)',
                  'rgba(75, 192, 192, 0.2)',
                  'rgba(153, 102, 255, 0.2)',
                  'rgba(255, 159, 64, 0.2)'
              ],
              borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
              ],
              borderWidth: 1
            }
          ] 
        },
        chartOptions: {
          responsive: true,
          scales: {
            y: {
                beginAtZero: true
            }
          }
        }
      },
    }
  }
}
</script>

<style>

</style>