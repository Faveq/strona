<script setup lang="ts">
import { BarChart } from '@/components/ui/chart-bar'

const data = [
  { name: '01 May', total: Math.floor(Math.random() * 100) + 500},
  { name: '02 May', total: Math.floor(Math.random() * 100) + 500},
  { name: '03 May', total: Math.floor(Math.random() * 100) + 500},
  { name: '04 May', total: Math.floor(Math.random() * 100) + 500},
  { name: '05 May', total: Math.floor(Math.random() * 100) + 500},
  { name: '06 May', total: Math.floor(Math.random() * 100) + 500},
  { name: '07 May', total: Math.floor(Math.random() * 100) + 500},
]
</script>

<template>
  <BarChart
    :data="data"
    index="name"
    :categories="['total', 'predicted']"
    :y-formatter="(tick: any) => {
      return typeof tick === 'number'
        ? `$ ${new Intl.NumberFormat('us').format(tick).toString()}`
        : ''
    }"
  />
</template>