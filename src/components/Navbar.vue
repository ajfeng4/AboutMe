<template>
  <v-app-bar flat color="white">
    <v-container>
      <v-row align="center" justify="space-between">
        <v-row align="center">
          <v-icon class="mr-3">mdi-account</v-icon>
          <span class="font-weight-bold">Alex Feng</span>
        </v-row>

        <v-row class="align-center">
          <v-btn text v-for="item in navItems" :key="item.text" :href="item.link">
            {{ item.text }}
          </v-btn>
        </v-row>

        <v-btn color="black" dark>
          Resume <v-icon right>mdi-download</v-icon>
        </v-btn>
      </v-row>
    </v-container>
  </v-app-bar>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      navItems: [
        { text: 'About Me', link: '#about' },
        { text: 'Skills', link: '#skills' },
        { text: 'Education', link: '#about' },
        { text: 'Experience', link: '#about' },
        { text: 'Projects', link: '#project' },
        { text: 'Contact Me', link: '#contact' },
      ],
    };
  },
};
</script>

<style scoped>
.v-btn {
  margin: 0 10px;
}
</style>