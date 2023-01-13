<template>
  <div>
    <h1>Chart.js</h1>
    <bar-chart :propsdata="chartDataSet" ></bar-chart>
    <line-chart></line-chart>
  </div>
</template>

<script>
import BarChart from '@/components/BarChart.vue';
import LineChart from './components/LineChart.vue';

export default {
  components:{
    BarChart,
    LineChart
  },
  data(){
    return{
      data :[
        { year: 2010, count: 10 },
        { year: 2011, count: 20 },
        { year: 2012, count: 15 },
        { year: 2013, count: 25 },
        { year: 2014, count: 22 },
        { year: 2015, count: 30 },
        { year: 2016, count: 28 },
      ],
    }
  },
  computed:{
    chartLabels(){
      return this.data.map(row => row.year);
    },
    chartDataSet(){
      return [
        {
          label: 'Acquisitions by year',
          data: this.data.map(row => row.count),
        }
      ]
    }
  },
  mounted(){

  }
}
</script>

<style>

</style>