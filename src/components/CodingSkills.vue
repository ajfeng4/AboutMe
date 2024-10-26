<template>
  <v-container class="text-center my-10">
    <h2 class="display-2 font-weight-bold">My Skills</h2>
    <v-row>
      <v-col
          v-for="(skill, index) in skills"
          :key="index"
          cols="6"
          md="3"
          class="d-flex justify-center"
      >
        <v-card outlined max-width="150" class="pa-4">
          <v-icon :size="50">{{ skill.icon }}</v-icon>
          <h3 class="mt-3">{{ skill.name }}</h3>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'CodingSkills',
  data() {
    return {
      skills: [
        { name: 'Git', icon: 'mdi-git' },
        { name: 'JavaScript', icon: 'mdi-language-javascript' },
        { name: 'Sass/SCSS', icon: 'mdi-sass' },
      ],
    };
  },
};
</script>

<style scoped>
.v-card {
  transition: transform 0.3s;
}
.v-card:hover {
  transform: scale(1.05);
}
</style>
