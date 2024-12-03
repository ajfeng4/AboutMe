<template>
  <v-card flat>
    <h1 class="display-2 font-weight-bold mb-3">Hello, I'm Alex Feng</h1>
    <h2 class="headline font-weight-bold">Software Engineer</h2>
    <SocialMedia />
  </v-card>
</template>

<script>
import SocialMedia from '../components/SocialMedia.vue';

export default {
  name: 'Landing',
  components: {
    SocialMedia,
  },
};
</script>

<style scoped>
</style>