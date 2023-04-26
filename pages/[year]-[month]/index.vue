<script setup lang="ts">
const route = useRoute();
const endpoint = computed(
  () => `/api/${route.params.year}-${route.params.month}`
);
const { data } = await useFetch(endpoint.value);
</script>

<template>
  <div>
    <h1>route.params</h1>
    <pre>{{ route.params }}</pre>
    <h1>response (actual)</h1>
    <pre>{{ data }}</pre>
    <h1>response (expected)</h1>
    <pre>{{ route.params }}</pre>
  </div>
  <ul>
    <li><NuxtLink :to="endpoint">endpoint</NuxtLink></li>
    <li><NuxtLink :to="{ name: 'index' }">index</NuxtLink></li>
  </ul>
</template>
