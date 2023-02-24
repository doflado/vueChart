<script>
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
import { Doughnut } from 'vue-chartjs'
import * as chartConfig from './chartConfig.ts'

ChartJS.register(ArcElement, Tooltip, Legend)

export default {
  name: 'App',
  components: {
    Doughnut
  },
  data() {
    return chartConfig
  }
}
</script>
  

<template>
    <div class="graphPanel">
        <Doughnut :data="data" :options="options" style="width: 600px;"/>
    </div>
</template>

<style scoped>

.graphPanel{
    margin-top: 125px;
    margin-bottom: 65px;
    width: 600px;
    height: 600px;
    background-image: url("../../assets/images/total/Vector.png");
    background-repeat: no-repeat;
    background-position-x: 50%;
    background-position-y: 50%;
}
.graphPage{
    display: flex;
    flex-direction: column;
}


</style>

