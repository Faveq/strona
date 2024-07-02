<script setup lang="ts">
import { DonutChart } from '@/components/ui/chart-donut'

const data = [
  { name: 'Percentage discount', total: Math.floor(Math.random() * 2000) + 500, predicted: Math.floor(Math.random() * 2000) + 500 },
  { name: 'Fixed card discounts', total: Math.floor(Math.random() * 2000) + 500, predicted: Math.floor(Math.random() * 2000) + 500 },
  { name: 'Fixed product discount', total: Math.floor(Math.random() * 2000) + 500, predicted: Math.floor(Math.random() * 2000) + 500 },
]
</script>

<template>
  <DonutChart
    index="name"
    :category="'total'"
    :data="data"
  />
</template>