<template>
  <div class="flex-col gap-3 h-svh bg-background relative content">
    <FirstPanel />
    <SecondPanel/>
    <ThirdPanel />
  </div>
</template>

<script setup lang="ts">
import FirstPanel from "./firstPanel/FirstPanel.vue";
import SecondPanel from "./secondPanel/SecondPanel.vue";
import ThirdPanel from "./thirdPanel/ThirdPanel.vue";
</script>

<style scoped>
.content{
margin-left:  150pt;
}    
</style>
