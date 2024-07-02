<template>
  <div class="flex-col gap-3 h-svh bg-background relative content">
    <FirstPanel />
    <SecondPanel/>
  </div>
</template>

<script setup lang="ts">
import FirstPanel from "./firstPanel/FirstPanel.vue";
import SecondPanel from "./secondPanel/SecondPanel.vue";
</script>

<style scoped>
.content{
margin-left:  150pt;
}    
</style>
