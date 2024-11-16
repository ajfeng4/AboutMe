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
    <Icon :icon="icon" width="20" height="20" color="white" />
    <span style="color: white; margin-left: 8px;">{{ text }}</span>
  </a>
</template>

<style scoped>
.link-button {
  display: inline-flex;
  align-items: center;
  padding: 9px;
  border-radius: 30px;
  margin-left: 1px;
  text-decoration: none;
}
</style>
