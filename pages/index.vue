<template>
  <main class="page page--index">
    <akContainer />
    <h2>歡迎使用 BProud Fronstage Template</h2>
  </main>
</template>

<script setup lang="ts">
const runtimeConfig = useRuntimeConfig()
const pageTitle = ref('Home Page')

useHead({
  title: pageTitle,
  meta: [
    {
      hid: 'og:title',
      property: 'og:title',
      content: pageTitle.value + ' - ' + runtimeConfig.public.websiteName
    },
    {
      hid: 'twitter:title',
      name: 'twitter:title',
      content: pageTitle.value + ' - ' + runtimeConfig.public.websiteName
    }
  ]
})
</script>
