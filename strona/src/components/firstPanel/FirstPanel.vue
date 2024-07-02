<template>
  <div class="flex content p-10 border-solid border-accent border relative">
    <div class="w-1/2">
      <p class="text-3xl font-extrabold">Ecommerce Dashboard</p>
      <p class="text-secondary">
        Here’s what’s going on at your business right now
      </p>
      <div class="flex mt-12">
        <GeneralOverview
          heading="57 new orders"
          desription="Awating processing"
          :icon="Star"
          color="green"
        />
        <GeneralOverview
          heading="5 orders"
          desription="On hold"
          :icon="Pause"
          color="orange"
        />
        <GeneralOverview
          heading="15 products"
          desription="Out of stock"
          :icon="X"
          color="red"
        />
      </div>
      <hr class="my-6" />
      <div class="flex-col">
        <p class="font-extrabold text-xl">Total sells</p>
        <p class="text-secondary">Payment received across all channels</p>
        <Chart class="w-full"/>
      </div>
    </div>
    <ChartsGroup class="w-1/2" />
  </div>
</template>

<script setup lang="ts">
import GeneralOverview from "./GeneralOverview.vue";
import Chart from "./Chart.vue";
import { Star, Pause, X } from "lucide-vue-next";
import ChartsGroup from "./ChartsGroup.vue";
</script>

<style scoped>
.content {
  margin: 0px !important;
}
@media only screen and (max-width: 1500px) {
  .content {
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    width: 100%;
    margin-left: 0px;
    padding: 2rem;
  }
}
</style>
