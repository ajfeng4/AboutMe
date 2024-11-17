<script setup>
import { Icon } from '@iconify/vue';
defineProps({
  icon: String,
  text: String,
  href: String,
  color: String,
});
</script>

<template>
  <a :href="href" target="_blank" class="link-button" :style="{ backgroundColor: color }">
    <Icon :icon="icon" width="16" height="16" color="white" />
    <span class="link-text">{{ text }}</span>
  </a>
</template>

<style scoped>
.link-button {
  display: flex;
  align-items: center;
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
  text-decoration: none;
  font-size: 0.85rem;
}

.link-text {
  color: white;
}
</style>
