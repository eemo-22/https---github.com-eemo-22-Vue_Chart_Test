<template>
  <!-- <Bar /> -->
  <Bar
    :chart-options="chartOptions"
    :chart-data="chartData"
    :chart-id="chartId"
    :dataset-id-key="datasetIdKey"
    :plugins="plugins"
    :css-classes="cssClasses"
    :styles="styles"
    :width="width"
    :height="height"
  />
</template>

<script>
import { Bar } from 'vue-chartjs';
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js';

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);

export default {
  name: 'BarChart',
  components: {
    Bar
  },
  //  왜 props 받으려고 하면 내려오지 않지? 왜 주석해야 적용됨?
  //  ㅎㅎ 알았음 템플릿에 바인딩 항목들 주석해버려서 그랬음
  //  Bar 자체가 chartJS가 제공하는 컴포넌트니까...
  props: {
    chartId: {
      type: String,
      default: 'bar-chart'
    },
    datasetIdKey: {
      type: String,
      default: 'label'
    },
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 400
    },
    cssClasses: {
      type: String,
      default: '',
    },
    plugins: {
      type: Object,
      default: () => {}
    }
  },
}
</script>

<style>

</style>