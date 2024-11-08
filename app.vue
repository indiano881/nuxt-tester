<template>
  <div>
    <NuxtPage />  
    <Navigation />
    <h1 class="text-2xl font-bold text-red-200">My first nuxt</h1>
    <NuxtRouteAnnouncer />
  </div>
</template>
<script setup lang="ts">
useHead({
  title: 'Mastermind 3.0',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  bodyAttrs: {
    class: 'test'
  },
  script: [ { innerHTML: 'console.log(\'Hello world\')' } ]
})
</script>
