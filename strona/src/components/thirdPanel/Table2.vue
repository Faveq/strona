<template>
    <Table>
      <TableHeader>
        <TableRow>
          <TableHead class="w-[200px]">COUNTRY</TableHead>
          <TableHead>USERS</TableHead>
          <TableHead> TRANSACTIONS </TableHead>
          <TableHead class="w-[300px]"> REVENUE </TableHead>
          <TableHead> CONV. RATE </TableHead>
        </TableRow>
      </TableHeader>
      <TableBody>
        <TableRow v-for="country in countries">
          <TableCell>
            <div class="flex items-center gap-1">
              <img
                src="/Images/flag.png"
                class="w-8 h-5"
                alt="hardware photo"
              />
              {{ country.country }}
            </div>
          </TableCell>
          <TableCell>

              {{ country.users }}
          </TableCell>
          <TableCell>
              {{ country.transactions }}
          </TableCell>
          <TableCell>
            {{ country.revenue }}
          </TableCell>
          <TableCell>
              {{country.rate}}
          </TableCell>
        </TableRow>
      </TableBody>
    </Table>
  </template>
  
  <script setup lang="ts">
  import {
    Table,
    TableBody,
    TableCell,
    TableHead,
    TableHeader,
    TableRow,
  } from "@/components/ui/table";
  
  const countries = [
    {
      country: 'India',
      users: 92838,
      transactions: 234,
      revenue: '$34333',
      rate: '1.54%'
    },{
      country: 'India',
      users: 92838,
      transactions: 234,
      revenue: '$34333',
      rate: '1.54%'
    },{
      country: 'India',
      users: 92838,
      transactions: 234,
      revenue: '$34333',
      rate: '1.54%'
    },{
      country: 'India',
      users: 92838,
      transactions: 234,
      revenue: '$34333',
      rate: '1.54%'
    },{
      country: 'India',
      users: 92838,
      transactions: 234,
      revenue: '$34333',
      rate: '1.54%'
    }
  ];
  </script>
  
  <style scoped></style>
  