<template>
  <div class="p-10 border-solid border-accent border relative">
    <p class="text-3xl font-extrabold">Top regions by revenue</p>
    <p class="text-secondary">Where you generated most of the revenue</p>
    <div class="flex content">
      <Table2 class="relative mt-8" />
      <img
        src="/Images/map.png"
        class="w-1/2 h-[450px] relative"
        alt="hardware photo"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import Table2 from "./Table2.vue";
import { Map } from "lucide-vue-next";
</script>

<style scoped>

@media only screen and (max-width: 1500px) {
  .content {
    flex-direction: column;
    align-items: center;
    gap: 2rem;
  }
}
</style>
