<template>
  <v-container>
    <v-row align="center" justify="center" class="my-10">
      <v-col cols="12" md="6">
        <v-card flat>
          <h1 class="display-2 font-weight-bold mb-3">Hello, I'm Alex Feng</h1>
          <h2 class="headline font-weight-bold">Software Engineer</h2>
          <h3 class="subheading font-weight-bold mb-3">Brooklyn, New York</h3>

          <p class="body-1 mb-4">
            A full time student taking an whole course load and working 40 hours a week. Passionate about front-end and mobile development,
            with experience in technical and non-technical environments. A experienced team player and seasoned leader.
          </p>

          <!-- Social Icons -->
          <v-row class="mb-4" align="center">
            <v-btn icon>
              <v-icon>mdi-github</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-linkedin</v-icon>
            </v-btn>
          </v-row>
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
export default {
  name: 'HelloWorld',
};
</script>

<style scoped>
.v-btn {
  margin-right: 10px;
}
</style>
