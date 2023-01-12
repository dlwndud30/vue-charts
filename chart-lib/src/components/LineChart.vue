<template>
  <div>
    <canvas id="lineChart"></canvas>
  </div>
</template>

<script>
import Chart from 'chart.js/auto';
export default {
    mounted(){
        const ctx = document.getElementById('lineChart');

        new Chart(ctx, {
            type: 'line',
            data: {
            labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
            datasets: [{
                label: '# of Votes',
                data: [12, 19, 3, 5, 2, 3],
                borderWidth: 1
            }]
            },
            options: {
            scales: {
                y: {
                beginAtZero: true
                }
            }
            }
        });
    }
}
</script>

<style>

</style>