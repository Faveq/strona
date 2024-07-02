<template>
  <div class="header flex justify-between p-2 px-5 border-solid border-accent border fixed z-50 w-full h-16 bg-white">
    <p class="text-3xl">Strona</p>
    <Command class="w-500">
      <CommandInput placeholder="Search"  />
    </Command>
    <div class="flex gap-3">
      <Sun color="gold" class="cursor-pointer"/>
      <Bell color="gray" class="cursor-pointer"/>
      <Menu color="gray" class="cursor-pointer"/>
      <CircleUser color="gray" class="cursor-pointer"/>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Command, CommandInput } from "@/components/ui/command";
import { Sun, Bell, Menu, CircleUser } from "lucide-vue-next";
</script>

<style scoped>
.header{
 align-items: center;   
}
</style>
