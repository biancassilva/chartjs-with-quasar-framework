<template>
  <q-card class="bg-white full-width">
    <q-card-section class="bg-blue-grey-8">
      <div class="row items-center no-wrap">
        <div class="col">
          <div class="text-h6 text-white text-center">Bubble Chart</div>
        </div>
      </div>
    </q-card-section>
    <q-card-section>
      <canvas id="bubble-chart"></canvas>
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
    this.createChart('bubble-chart')
  },
  methods: {
    createChart (chartId) {
      const ctx = document.getElementById(chartId)
      const myChart = new Chart(ctx, {
        type: 'bubble',
        data: {
          labels: 'Africa',
          datasets: [
            {
              label: ['China'],
              backgroundColor: 'rgba(255,221,50,0.2)',
              borderColor: 'rgba(255,221,50,1)',
              data: [{
                x: 21269017,
                y: 5.245,
                r: 15
              }]
            }, {
              label: ['Denmark'],
              backgroundColor: 'rgba(60,186,159,0.2)',
              borderColor: 'rgba(60,186,159,1)',
              data: [{
                x: 258702,
                y: 7.526,
                r: 10
              }]
            }, {
              label: ['Germany'],
              backgroundColor: 'rgba(0,0,0,0.2)',
              borderColor: '#000',
              data: [{
                x: 3979083,
                y: 6.994,
                r: 15
              }]
            }, {
              label: ['Japan'],
              backgroundColor: 'rgba(193,46,12,0.2)',
              borderColor: 'rgba(193,46,12,1)',
              data: [{
                x: 4931877,
                y: 5.921,
                r: 15
              }]
            }
          ]
        },
        options: {
          title: {
            display: true,
            text: 'Predicted world population (millions) in 2050'
          },
          scales: {
            yAxes: [{
              scaleLabel: {
                display: true,
                labelString: 'Happiness'
              }
            }],
            xAxes: [{
              scaleLabel: {
                display: true,
                labelString: 'GDP (PPP)'
              }
            }]
          }
        }
      })
      return myChart
    }
  }
}
</script>

<style>
</style>
