<template>
  <v-container>
    <v-row align="center" justify="center" class="my-10">
      <v-col cols="12" md="6">
        <v-form>
          <v-text-field label="Full Name" outlined class="mb-4"></v-text-field>
          <v-text-field label="Email Address" outlined class="mb-4"></v-text-field>
          <v-textarea label="Your Message" outlined rows="5" class="mb-6"></v-textarea>
          <v-btn block color="primary" class="mb-4">Contact Me</v-btn>
          <v-row justify="center">
            <v-btn icon><v-icon>mdi-facebook</v-icon></v-btn>
            <v-btn icon><v-icon>mdi-twitter</v-icon></v-btn>
            <v-btn icon><v-icon>mdi-instagram</v-icon></v-btn>
            <v-btn icon><v-icon>mdi-linkedin</v-icon></v-btn>
          </v-row>
        </v-form>
      </v-col>
      <v-col cols="12" md="6" class="text-center">
        <h1 class="display-1 font-weight-bold">Connect with Me</h1>
        <p class="body-1 mb-6">
          Contact me!
        </p>
        <p class="body-1">
          Email: <br>
          Phone:
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'ContactMe',
};
</script>

<style scoped>
.v-btn {
  margin: 0 10px;
}
</style>
