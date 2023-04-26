<script setup lang="ts"></script>

<template>
  <ul>
    <li>
      <NuxtLink :to="{ name: 'year-month', params: { year: 2023, month: 4 } }"
        >2023-4</NuxtLink
      >
    </li>
    <li>
      <NuxtLink :to="{ name: 'year-month', params: { year: 2023, month: 5 } }"
        >2023-5</NuxtLink
      >
    </li>
  </ul>
</template>
