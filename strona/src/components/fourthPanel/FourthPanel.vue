<template>
  <div
    class="flex content p-10 gap-4 border-solid border-accent border relative"
  >
    <LeftChart class="w-1/2" />
    <RightChart class="w-1/2" />
  </div>
</template>

<script setup lang="ts">
import LeftChart from "./LeftChart.vue";
import RightChart from "./RightChart.vue";
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
  }
}
</style>
