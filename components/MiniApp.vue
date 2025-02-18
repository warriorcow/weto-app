<script lang="ts" setup>
import { MainButton, useWebAppPopup, useWebAppViewport } from 'vue-tg'

const { showAlert } = useWebAppPopup()
const viewport = useWebAppViewport();

onMounted(() => {
  console.log('onMounted')
  viewport.expand();
})
</script>

<template>
  <MainButton text="Open alert" @click="() => showAlert('Hello!')" />
</template>