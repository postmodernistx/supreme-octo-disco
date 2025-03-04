<script setup>
import { ref } from 'vue';

import MenuButton from '@/components/atoms/MenuButton.vue';

const showNav = ref(false);

function toggleNav() {
  showNav.value = !showNav.value;
}
</script>

<template>
  <header>
    <MenuButton class="toggle-menu" @change="toggleNav" />

    <h1>Landing page</h1>

    <button class="buy-now">Buy now</button>

    <p>Menyn öppen: {{ showNav }}</p>

    <nav>
      <ul>
        <li>Home</li>
        <li>About</li>
        <li>Contact</li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss" scoped>
@import 'header.scss';
</style>