<script setup lang="ts">
import MainHeader from '@/fixtures/header/MainHeader.vue';
import IconButton from '@/components/atoms/IconButton.vue'
</script>

<template>
  <MainHeader />

  <IconButton button-text="Köp nu!" />
  <IconButton button-text="Köp genast!" icon="🛒" />

  <!-- <RouterView /> -->
  <!-- <MainFooter />-->
</template>

<style scoped>
</style>
