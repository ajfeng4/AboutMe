<template>
  <v-app>
    <Navbar />
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar.vue';

export default {
  name: 'App',
  components: {
    Navbar,
  },
};
</script>

<style>
html {
  font-size: 16px;
  zoom: 1;
  -webkit-text-size-adjust: 100%;
  -ms-text-size-adjust: 100%;
}

body {
  margin: 0;
  padding: 0;
  font-family: 'Roboto', sans-serif;
}

* {
  box-sizing: border-box;
}
</style>
