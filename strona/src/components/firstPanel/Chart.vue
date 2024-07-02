<template>
  <LineChart
    :data="data"
    index="year"
    :categories="['Card', 'Cash']"
    :y-formatter="(tick: any) => {
      return typeof tick === 'number'
        ? `$ ${new Intl.NumberFormat('us').format(tick).toString()}`
        : ''
    }"
  />
</template>
<script setup lang="ts">
import { LineChart } from "@/components/ui/chart-line";

const data = [
  {
    year: 1970,
    "Card": 2.04,
    "Cash": 1.53,
  },
  {
    year: 1971,
    "Card": 1.96,
    "Cash": 1.58,
  },
  {
    year: 1972,
    "Card": 1.96,
    "Cash": 1.61,
  },
  {
    year: 1973,
    "Card": 1.93,
    "Cash": 1.61,
  },
  {
    year: 1974,
    "Card": 1.88,
    "Cash": 1.67,
  },
  {
    year: 1975,
    "Card": 1.79,
    "Cash": 1.64,
  },
  {
    year: 1976,
    "Card": 1.77,
    "Cash": 1.62,
  },
  {
    year: 1977,
    "Card": 1.74,
    "Cash": 1.69,
  },
  {
    year: 1978,
    "Card": 1.74,
    "Cash": 1.7,
  },
  {
    year: 1979,
    "Card": 1.77,
    "Cash": 1.67,
  },
  {
    year: 1980,
    "Card": 1.79,
    "Cash": 1.7,
  },
  {
    year: 1981,
    "Card": 1.81,
    "Cash": 1.72,
  },
  {
    year: 1982,
    "Card": 1.84,
    "Cash": 1.73,
  },
  {
    year: 1983,
    "Card": 1.77,
    "Cash": 1.73,
  },
  {
    year: 1984,
    "Card": 1.78,
    "Cash": 1.78,
  },
  {
    year: 1985,
    "Card": 1.78,
    "Cash": 1.81,
  },
  {
    year: 1986,
    "Card": 1.82,
    "Cash": 1.89,
  },
  {
    year: 1987,
    "Card": 1.82,
    "Cash": 1.91,
  },
  {
    year: 1988,
    "Card": 1.77,
    "Cash": 1.94,
  },
  {
    year: 1989,
    "Card": 1.76,
    "Cash": 1.94,
  },
  {
    year: 1990,
    "Card": 1.75,
    "Cash": 1.97,
  },
  {
    year: 1991,
    "Card": 1.62,
    "Cash": 1.99,
  },
  {
    year: 1992,
    "Card": 1.56,
    "Cash": 2.12,
  },
  {
    year: 1993,
    "Card": 1.5,
    "Cash": 2.13,
  },
  {
    year: 1994,
    "Card": 1.46,
    "Cash": 2.15,
  },
  {
    year: 1995,
    "Card": 1.43,
    "Cash": 2.17,
  },
  {
    year: 1996,
    "Card": 1.4,
    "Cash": 2.2,
  },
  {
    year: 1997,
    "Card": 1.37,
    "Cash": 2.15,
  },
  {
    year: 1998,
    "Card": 1.34,
    "Cash": 2.07,
  },
  {
    year: 1999,
    "Card": 1.32,
    "Cash": 2.05,
  },
  {
    year: 2000,
    "Card": 1.33,
    "Cash": 2.07,
  },
  {
    year: 2001,
    "Card": 1.31,
    "Cash": 2.08,
  },
  {
    year: 2002,
    "Card": 1.29,
    "Cash": 2.1,
  },
  {
    year: 2003,
    "Card": 1.27,
    "Cash": 2.15,
  },
  {
    year: 2004,
    "Card": 1.27,
    "Cash": 2.21,
  },
  {
    year: 2005,
    "Card": 1.26,
    "Cash": 2.23,
  },
  {
    year: 2006,
    "Card": 1.26,
    "Cash": 2.29,
  },
  {
    year: 2007,
    "Card": 1.27,
    "Cash": 2.34,
  },
  {
    year: 2008,
    "Card": 1.26,
    "Cash": 2.36,
  },
  {
    year: 2009,
    "Card": 1.26,
    "Cash": 2.36,
  },
  {
    year: 2010,
    "Card": 1.25,
    "Cash": 2.35,
  },
  {
    year: 2011,
    "Card": 1.24,
    "Cash": 2.34,
  },
  {
    year: 2012,
    "Card": 1.25,
    "Cash": 2.39,
  },
  {
    year: 2013,
    "Card": 1.22,
    "Cash": 2.3,
  },
  {
    year: 2014,
    "Card": 1.2,
    "Cash": 2.35,
  },
  {
    year: 2015,
    "Card": 1.17,
    "Cash": 2.39,
  },
  {
    year: 2016,
    "Card": 1.16,
    "Cash": 2.41,
  },
  {
    year: 2017,
    "Card": 1.13,
    "Cash": 2.44,
  },
  {
    year: 2018,
    "Card": 1.07,
    "Cash": 2.45,
  },
  {
    year: 2019,
    "Card": 1.03,
    "Cash": 2.47,
  },
  {
    year: 2020,
    "Card": 0.92,
    "Cash": 2.48,
  },
  {
    year: 2021,
    "Card": 0.82,
    "Cash": 2.51,
  },
];
</script>
