<template>
  <q-card class="bg-white full-width">
    <q-card-section class="bg-blue-grey-8">
      <div class="row items-center no-wrap">
        <div class="col">
          <div class="text-h6 text-white text-center">Radar Chart</div>
        </div>
      </div>
    </q-card-section>
    <q-card-section>
      <canvas id="radar-chart"></canvas>
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
    this.createChart('radar-chart')
  },
  methods: {
    createChart (chartId) {
      const ctx = document.getElementById(chartId)
      const myChart = new Chart(ctx, {
        type: 'radar',
        data: {
          labels: ['Africa', 'Asia', 'Europe', 'Latin America', 'North America'],
          datasets: [
            {
              label: '1950',
              fill: true,
              backgroundColor: 'rgba(179,181,198,0.2)',
              borderColor: 'rgba(179,181,198,1)',
              pointBorderColor: '#fff',
              pointBackgroundColor: 'rgba(179,181,198,1)',
              data: [8.77, 55.61, 21.69, 6.62, 6.82],
              borderWidth: 1.5
            }, {
              label: '2050',
              fill: true,
              backgroundColor: 'rgba(255,99,132,0.2)',
              borderColor: 'rgba(255,99,132,1)',
              pointBorderColor: '#fff',
              pointBackgroundColor: 'rgba(255,99,132,1)',
              data: [25.48, 54.16, 7.61, 8.06, 4.45],
              borderWidth: 1.5
            }
          ]
        },
        options: {
          title: {
            display: true,
            text: 'Distribution in % of world population'
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
