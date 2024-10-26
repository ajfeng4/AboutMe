<template>
  <v-container>
    <v-row align="center" justify="center" class="my-10">
      <!-- Profile Information Container -->
      <v-col cols="12" md="6">
        <v-card flat>
          <h1 class="display-2 font-weight-bold mb-3">Hello, I'm Alex Feng</h1>
          <h2 class="headline font-weight-bold">Software Engineer</h2>
          <h3 class="subheading font-weight-bold mb-3">Brooklyn, New York</h3>

          <p class="body-1 mb-4">
            A full time student taking a whole course load and working 40 hours a week. Passionate about front-end and mobile development,
            with experience in technical and non-technical environments. An experienced team player and seasoned leader.
          </p>

          <SocialMedia />
        </v-card>
      </v-col>

      <!-- Image Placeholder Container -->
      <v-col cols="12" md="6" class="text-center">
        <v-card flat>
          <v-icon size="150" color="grey">mdi-account-circle</v-icon>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import SocialMedia from '../components/SocialMedia.vue';

export default {
  name: 'HelloWorld',
  components: {
    SocialMedia,
  },
};
</script>
