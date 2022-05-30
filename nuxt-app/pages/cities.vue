<template>
  <div>
    <h1>Cities Page</h1>

    <div v-if="pending">Loading...</div>

    <div v-else>
      <p v-for="city in data.citiesData" :key="city.code">
        <NuxtLink :to="`/city-detail/${city.code}`">
          {{ city.name }} - {{ city.code }}
        </NuxtLink>
      </p>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  title: "Cities page title",
});

const { data, pending, error, refresh } = await useFetch(
  "https://mocki.io/v1/d83d0bf6-2798-4703-9273-93cac7a383b0"
);

// const citiesData = [
//   { name: "İstanbul", code: 34 },
//   { name: "Ankara", code: 6 },
//   { name: "İzmir", code: 35 },
// ];
</script>
