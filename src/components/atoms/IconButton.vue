<script setup lang="ts">
import { onMounted } from 'vue'

const props = defineProps({
  buttonText: { type: String, required: true },
  icon: { type: String, required: false },
});

onMounted(() => {
  if (props.icon) {
    console.log('Denna knapp har en ikon:', props.buttonText);
  }
});
</script>

<template>
  <button :class="{ 'has-icon': icon }">
    <span v-if="icon">{{ icon }}</span>
    {{ buttonText }}
  </button>
</template>

<style scoped lang="scss">
button {
  padding: 8px 16px;
  background: #2c3e50;
  color: #fff;
  border: 0;
  border-radius: 8px;
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
  cursor: pointer;
  transition: background 0.3s cubic-bezier(0.785, 0.135, 0.15, 0.86);

  &:hover {
    background: dodgerblue;
  }

  &.has-icon {
    background-color: antiquewhite;
    color: black;
  }
}

span {
  display: inline-block;
  margin-right: 4px;
}
</style>
