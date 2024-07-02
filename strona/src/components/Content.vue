<template>
  <div class="flex-col gap-3 h-svh bg-background relative content">
    <FirstPanel />
    <SecondPanel/>
    <ThirdPanel />
    <FourthPanel/>
    <Footer/>
  </div>
</template>

<script setup lang="ts">
import FirstPanel from "./firstPanel/FirstPanel.vue";
import SecondPanel from "./secondPanel/SecondPanel.vue";
import ThirdPanel from "./thirdPanel/ThirdPanel.vue";
import FourthPanel from "./fourthPanel/FourthPanel.vue";
import Footer from "./Footer.vue";
</script>

<style scoped>
.content{
margin-left:  150pt;
padding-top:  4rem;
}    
</style>
