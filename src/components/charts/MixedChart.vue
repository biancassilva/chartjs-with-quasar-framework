<template>
  <q-card class="bg-white full-width">
    <q-card-section class="bg-blue-grey-8">
      <div class="row items-center no-wrap">
        <div class="col">
          <div class="text-h6 text-white text-center">Mixed Chart</div>
        </div>
      </div>
    </q-card-section>
    <q-card-section>
      <canvas id="mixed-chart"></canvas>
    </q-card-section>
  </q-card>
</template>

<script>
import Chart from 'chart.js'
export default {
  data () {
    return {
    }
  },
  mounted () {
    this.createChart('mixed-chart')
  },
  methods: {
    createChart (chartId) {
      const ctx = document.getElementById(chartId)
      const myChart = new Chart(ctx, {
        type: 'bar',
        data: {
          labels: ['1900', '1950', '1999', '2050'],
          datasets: [{
            label: 'Europe',
            type: 'line',
            borderColor: '#8e5ea2',
            data: [408, 547, 675, 734],
            fill: false
          }, {
            label: 'Africa',
            type: 'line',
            borderColor: '#3e95cd',
            data: [133, 221, 783, 2478],
            fill: false
          }, {
            label: 'Europe',
            type: 'bar',
            backgroundColor: 'rgba(0,0,0,0.2)',
            data: [408, 547, 675, 734]
          }, {
            label: 'Africa',
            type: 'bar',
            backgroundColor: 'rgba(0,0,0,0.2)',
            backgroundColorHover: '#3e95cd',
            data: [133, 221, 783, 2478]
          }
          ]
        },
        options: {
          title: {
            display: true,
            text: 'Population growth (millions): Europe & Africa'
          },
          legend: { display: false }
        }
      })
      return myChart
    }
  }
}
</script>

<style>
</style>
