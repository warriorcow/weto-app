<script setup lang="ts">
import 'assets/style/index.css'
import MiniApp from '~/components/MiniApp.vue'
</script>

<template>
  <NuxtPage />
  <ClientOnly>
    <MiniApp />
  </ClientOnly>
</template>
