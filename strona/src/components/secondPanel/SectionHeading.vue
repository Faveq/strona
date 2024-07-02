<template>
  <div class="flex justify-between">
    <div class="flex-co">
      <p class="text-3xl font-extrabold">Latest reviews</p>
      <p class="text-secondary">Payment received across all channels</p>
    </div>
    <div class="flex items-baseline gap-2">
      <Command>
        <CommandInput placeholder="Search" class="w-40" />
      </Command>
      <Button> All products </Button>
      <DropdownMenu>
        <DropdownMenuTrigger><Button> ... </Button></DropdownMenuTrigger>
        <DropdownMenuContent>
          <DropdownMenuLabel>My Account</DropdownMenuLabel>
          <DropdownMenuSeparator />
          <DropdownMenuItem>Profile</DropdownMenuItem>
          <DropdownMenuItem>Billing</DropdownMenuItem>
          <DropdownMenuItem>Team</DropdownMenuItem>
          <DropdownMenuItem>Subscription</DropdownMenuItem>
        </DropdownMenuContent>
      </DropdownMenu>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Command, CommandInput } from "@/components/ui/command";
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuTrigger,
} from "@/components/ui/dropdown-menu";

import { Button } from "@/components/ui/button";
</script>

<style scoped></style>
