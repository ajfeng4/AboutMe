<template>
  <v-row class="mb-4" align="center">
    <v-btn icon v-for="(icon, index) in icons" :key="index">
      <v-icon>{{ icon }}</v-icon>
    </v-btn>
  </v-row>
</template>

<script>
export default {
  name: 'SocialMedia',
  data() {
    return {
      icons: ['mdi-github', 'mdi-twitter', 'mdi-facebook', 'mdi-linkedin'],
    };
  },
};
</script>

<style scoped>
.v-btn {
  margin-right: 10px;
}
</style>
