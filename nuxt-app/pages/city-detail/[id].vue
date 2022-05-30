<template>
  <div>
    <h1>City Detail - {{ $route.params.id }}</h1>

    <!-- <div>{{ JSON.stringify(route) }}</div> -->
  </div>
</template>

<script setup>
definePageMeta({
  title: "city detail",
});
</script>
