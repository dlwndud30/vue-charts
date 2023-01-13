<template>
  <div>
    <canvas ref="barChart" id="barChart" width="400" height="400"></canvas>
  </div>
</template>

<script>

export default {
  props:['propsdata'],
  mounted(){
    const ctx = this.$refs.barChart;
            new this.$_Chart(ctx, {
            type: 'bar',
            data: {
                labels: ['2010', '2011', '2012', '2013', '2014', '2015', '2016'],
                datasets: this.propsdata,
            },
            options: {
                scales: {
                    y: {
                    beginAtZero: true
                    }
                }
            }
        });

  },
}
</script>

<style>

</style>