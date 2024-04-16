<template>
  <main class="page">
    <akContainer />
    <h2>Vue-word-cloud</h2>
    <nuxt-link
      to="https://github.com/SeregPie/VueWordCloud"
      title="另開視窗前往 vue-word-cloud 套件網站"
      target="_blank"
      rel="noreferrer noopener"
    >
      vue-word-cloud github
    </nuxt-link>
    <vue-word-cloud
      style="height: 480px; width: 640px"
      :words="[
        ['romance', 19],
        ['horror', 3],
        ['fantasy', 7],
        ['adventure', 3]
      ]"
      :color="
        ([, weight]: [string, number]) =>
          weight > 10 ? 'DeepPink' : weight > 5 ? 'RoyalBlue' : 'Indigo'
      "
      font-family="Roboto"
    />
  </main>
</template>

<script setup lang="ts">
const { VueWordCloud } = useWordCloud()
</script>
