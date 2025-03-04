<script setup lang="ts">
import { ref } from 'vue';

const emit = defineEmits(['change']);

const isOpen = ref(false); // let isOpen = false;

function toggleOpen() {
  isOpen.value = !isOpen.value;

  emit('change');
}
</script>

<template>
  <button @click="toggleOpen">
    <span v-if="isOpen">Stäng</span>
    <span v-if="!isOpen">Öppna</span>
  </button>
</template>