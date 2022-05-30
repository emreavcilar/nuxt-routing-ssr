<template>
  <div>
    <header>
      <nav class="nav">
        <ul>
          <li>
            <NuxtLink to="/cities"> Cities </NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <NuxtPage />
  </div>
</template>

<script setup>
const route = useRoute();

useHead({
  // titleTemplate: "My App - %s",
  // or, instead:
  // titleTemplate: (title) => `My App - ${route.meta.title}`,
  title: `My App - ${route.meta.title}`,
  viewport: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
  meta: [{ name: "description", content: "Great City Listing App" }],
  bodyAttrs: {
    class: "test",
  },
});
</script>
