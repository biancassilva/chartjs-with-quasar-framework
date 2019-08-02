<template>
  <div class="row justify-center q-pa-lg">
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <bar-chart></bar-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <line-chart></line-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <radar-chart></radar-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <pie-chart></pie-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <polar-area-chart></polar-area-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <doughnut-chart></doughnut-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <horizontal-bar-chart></horizontal-bar-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <mixed-chart></mixed-chart>
    </div>
    <div class="col-xl-4 col-lg-6 col-md-6 col-sm-10 col-xs-12 q-pa-sm">
      <bubble-chart></bubble-chart>
    </div>
  </div>
</template>

<style>
</style>

<script>
import BarChart from '../components/charts/BarChart'
import LineChart from '../components/charts/LineChart'
import RadarChart from '../components/charts/RadarChart'
import PieChart from '../components/charts/PieChart'
import PolarAreaChart from '../components/charts/PolarAreaChart'
import DoughnutChart from '../components/charts/DoughnutChart'
import HorizontalBarChart from '../components/charts/HorizontalBarChart'
import MixedChart from '../components/charts/MixedChart'
import BubbleChart from '../components/charts/BubbleChart'
export default {
  name: 'PageIndex',
  components: {
    BarChart,
    LineChart,
    RadarChart,
    PieChart,
    PolarAreaChart,
    DoughnutChart,
    HorizontalBarChart,
    MixedChart,
    BubbleChart
  },
  data () {
    return {}
  }
}
</script>
