<template>
  <v-container>
    <v-row class="justify-space-between align-center py-6">
      <v-col cols="12" md="4" class="text-center text-md-left">
        <p class="caption">Updated November 17, 2024</p>
      </v-col>
      <v-col cols="12" md="4" class="text-center">
        <p class="caption">alexfeng@buffalo.edu</p>
      </v-col>
      <v-col cols="12" md="4" class="text-center text-md-right">
        <v-btn icon>
          <v-icon>mdi-github</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-camera</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-email</v-icon>
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Footer',
};
</script>

<style scoped>
.caption {
  color: #333;
  font-size: 14px;
  font-weight: 500;
}

.v-btn {
  color: #333;
}
</style>
