<template>
  <div class="cont">
    <div class="flex-col graph border-solid border-accent border p-4 rounded-md ">
      <p class="font-bold">Top coupons</p>
      <p class="text-secondary text-xs mb-7">Last 7 days</p>
      <DonutChart />
    </div>

    <div class="flex-col graph border-solid border-accent border  p-4 rounded-md ">
      <p class="font-bold">Paying vs non paying</p>
      <p class="text-secondary text-xs mb-7">Last 7 days</p>
      <DonutChart/>
    </div>

    <div class="flex-col graph border-solid border-accent border p-4 rounded-md overflow-hidden">
      <p class="font-bold">Total orders</p>
      <p class="text-secondary text-xs mb-7">Last 7 days</p>
      <BarChart />
    </div>

    <div class="flex-col graph border-solid border-accent border p-4 rounded-md h-fit ">
      <p class="font-bold">New customers</p>
      <p class="text-secondary text-xs mb-7">Last 7 days</p>
      <LineChart class="w-min h-min"/>
    </div>
  </div>
</template>

<script setup lang="ts">
import DonutChart from "./DonutChart.vue";
import BarChart from "./BarChart.vue";
import LineChart from "./LineChart.vue";


</script>

<style scoped>
.cont {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
  }
  
  .graph {
    min-width: 140px;
    height: 20rem;
    line-height: 24px;
    box-sizing: border-box;
  }
  
</style>
