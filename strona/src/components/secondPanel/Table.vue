<template>
  <Table>
    <TableHeader>
      <TableRow>
        <TableHead class="w-[100px]">
          <Checkbox />
        </TableHead>
        <TableHead class="w-[400px]">Product</TableHead>
        <TableHead>Customer</TableHead>
        <TableHead> Rating </TableHead>
        <TableHead class="w-[300px]"> Review </TableHead>
        <TableHead> Status </TableHead>
        <TableHead> Time </TableHead>
      </TableRow>
    </TableHeader>
    <TableBody>
      <TableRow v-for="invoice in invoices">
        <TableCell class="font-medium">
          <Checkbox />
        </TableCell>
        <TableCell>
          <div class="flex items-center gap-1">
            <img
              src="/Images/photo.png"
              class="w-12 h-12"
              alt="hardware photo"
            />
            {{ invoice.name }}
          </div>
        </TableCell>
        <TableCell>
          <div class="flex items-center gap-1">
            <img
              src="/Images/person.png"
              class="w-12 h-12 rounded-full"
              alt="hardware photo"
            />
            {{ invoice.customer }}
          </div>
        </TableCell>
        <TableCell>
            <div class="flex">
          <Star class="w-3 h-3" color="gold"/>
          <Star class="w-3 h-3" color="gold"/>
          <Star class="w-3 h-3" color="gold"/>
          <StarHalf class="w-3 h-3" color="gold"/>
        </div>
        </TableCell>
        <TableCell>
          {{ invoice.review }}
        </TableCell>
        <TableCell>
            <Badge variant="outline" class="border-green-700 bg-green-200">
                APPROVED
              </Badge>
        </TableCell>
        <TableCell>
          {{ invoice.time }}
        </TableCell>
      </TableRow>
    </TableBody>
  </Table>
</template>

<script setup lang="ts">
import {
  Table,
  TableBody,
  TableCaption,
  TableCell,
  TableHead,
  TableHeader,
  TableRow,
} from "@/components/ui/table";
import { Checkbox } from "@/components/ui/checkbox";
import { Star,StarHalf  } from 'lucide-vue-next';
import { Badge } from "@/components/ui/badge"

const invoices = [
  {
    name: '	Apple iMac 24" 4K Retina Display M1 8 Core CPU...',
    customer: "Eric McGee",
    review: "This Fitbit is fantastic! I was trying to be in better shape and needed some motivation, so I decided to treat myself to a new Fitbit.",
    time: "Just now",
  }, {
    name: '	Apple iMac 24" 4K Retina Display M1 8 Core CPU...',
    customer: "Eric McGee",
    review: "This Fitbit is fantastic! I was trying to be in better shape and needed some motivation, so I decided to treat myself to a new Fitbit.",
    time: "Just now",
  },
  {
    name: '	Apple iMac 24" 4K Retina Display M1 8 Core CPU...',
    customer: "Eric McGee",
    review: "This Fitbit is fantastic! I was trying to be in better shape and needed some motivation, so I decided to treat myself to a new Fitbit.",
    time: "Just now",
  },
  {
    name: '	Apple iMac 24" 4K Retina Display M1 8 Core CPU...',
    customer: "Eric McGee",
    review: "This Fitbit is fantastic! I was trying to be in better shape and needed some motivation, so I decided to treat myself to a new Fitbit.",
    time: "Just now",
  },
];
</script>

<style scoped></style>
