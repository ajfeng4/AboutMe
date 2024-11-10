<template>
  <v-app-bar flat color="white">
    <v-container>
      <v-row align="center" justify="space-between">
        <v-row align="center">
          <v-icon class="mr-3">mdi-account</v-icon>
          <span class="font-weight-bold">Alex Feng</span>
        </v-row>

        <v-row class="align-center">
          <v-btn text v-for="item in navItems" :key="item.text" @click="scrollToSection(item.link)">
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
        { text: 'About Me', link: 'about' },
        { text: 'Skills', link: 'skills' },
        { text: 'Education', link: 'education' },
        { text: 'Experience', link: 'experience' },
        { text: 'Projects', link: 'projects' },
        { text: 'Contact Me', link: 'contact' },
      ],
    };
  },
  methods: {
    scrollToSection(id) {
      const element = document.getElementById(id);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>

<style scoped>
.v-btn {
  margin: 0 10px;
}
</style>