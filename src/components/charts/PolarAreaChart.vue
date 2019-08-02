<template>
  <q-card class="bg-white full-width">
    <q-card-section class="bg-blue-grey-8">
      <div class="row items-center no-wrap">
        <div class="col">
          <div class="text-h6 text-white text-center">Polar Area Chart</div>
        </div>
      </div>
    </q-card-section>
    <q-card-section>
      <canvas id="polar-area-chart"></canvas>
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
    this.createChart('polar-area-chart')
  },
  methods: {
    createChart (chartId) {
      const ctx = document.getElementById(chartId)
      const myChart = new Chart(ctx, {
        type: 'polarArea',
        data: {
          labels: ['Africa', 'Asia', 'Europe', 'Latin America', 'North America'],
          datasets: [
            {
              label: 'Population (millions)',
              backgroundColor: ['#3e95cd', '#8e5ea2', '#3cba9f', '#e8c3b9', '#c45850'],
              data: [2478, 5267, 734, 784, 433]
            }
          ]
        },
        options: {
          title: {
            display: true,
            text: 'Predicted world population (millions) in 2050'
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
