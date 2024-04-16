<template>
  <main class="page">
    <h3>巢狀頁面內頁</h3>
    <ul>
      <li v-for="(itemm, index) in 50" :key="index">
        <nuxt-link to="/">Item</nuxt-link>
      </li>
    </ul>
  </main>
</template>
