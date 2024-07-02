<template>
  <div class="overCard flex items-center mx-3">
    <component :is="props.icon" class="h-11 w-11 m-1" :color="props.color"/>
    <div class="flex-col">
      <p class="font-semibold text-xl">{{ props.heading }}</p>
      <p class="text-secondary text-sm">{{ props.desription }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { DefineComponent } from "vue";
import { LucideProps } from "lucide-vue-next";

const props = defineProps({
  heading: {
    type: String,
  },
  desription: {
    type: String,
  },
  icon: {
    type: Object as () => LucideProps,
  },
  color:{
    type: String
  }
});
</script>

<style scoped></style>
