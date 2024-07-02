<template>
<div class="w-screen">
<Nav />
<Content />
</div>
</template>

<script setup lang="ts">
import Nav from './components/Nav.vue';
import Content from './components/Content.vue';
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&display=swap');
.nunito-sans-light {
    font-family: "Nunito Sans", sans-serif;
    font-optical-sizing: auto;
    font-weight: 400;
    font-style: normal;
    font-variation-settings:
      "wdth" 100,
      "YTLC" 500;
  }
*{
    font-family: Nunito Sans;
}
</style>
