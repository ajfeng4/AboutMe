<template>
  <v-container class="text-center my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Skills</span>
    </h2>
    <v-row justify="space-between" align="center">
      <v-col
          v-for="(skill, index) in skills"
          :key="index"
          cols="2"
          sm="3"
          md="2"
          class="d-flex justify-center"
      >
        <v-card
            outlined
            elevation="2"
            class="skill-card pa-4 d-flex flex-column align-center"
            width="100%"
        >
          <template v-if="isMdiIcon(skill.icon)">
            <v-icon :size="80" class="mb-2" :style="{ color: skill.color }">
              {{ skill.icon }}
            </v-icon>
          </template>
          <template v-else>
            <i :class="[skill.icon, 'boxicon-size']" :style="{ color: skill.color }"></i>
          </template>
          <span class="font-weight-medium">{{ skill.name }}</span>
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
        { name: 'TypeScript', icon: 'mdi-language-typescript', color: '#007acc' },
        { name: 'JavaScript', icon: 'mdi-language-javascript', color: '#f0db4f' },
        { name: 'CSS', icon: 'bx bxl-css3', color: '#264de4' },
        { name: 'HTML', icon: 'bx bxl-html5', color: '#e34c26' },
        { name: 'React.js', icon: 'mdi-react', color: '#f0db4f' },
        { name: 'React Native', icon: 'mdi-react', color: '#61dafb' },
        { name: 'Vue.js', icon: 'mdi-vuejs', color: '#42b883' },
        { name: 'Angular', icon: 'bx bxl-angular', color: '#dd0031' },
        { name: 'Node.js', icon: 'mdi-nodejs', color: '#43853d' },
        { name: 'Python', icon: 'bx bxl-python', color: '#3776ab' },
        { name: 'Java', icon: 'bx bxl-java', color: '#007396' },
        { name: 'C++', icon: 'bx bxl-c-plus-plus', color: '#00599c' },
        { name: 'Spring Boot', icon: 'bx bxl-spring-boot', color: '#6db33f' },
        { name: 'SQL', icon: 'bx bxs-data', color: '#e38c00' },
        { name: 'PostgreSQL', icon: 'bx bxl-postgresql', color: '#336791' },
        { name: 'Firebase', icon: 'bx bxl-firebase', color: '#ffca28' },
        { name: 'Supabase', icon: 'bx bxl-supabase', color: '#3ecf8e' },
        { name: 'Git', icon: 'mdi-git', color: '#f34f29' }
      ],
    };
  },
  methods: {
    isMdiIcon(icon) {
      return icon.startsWith('mdi-');
    },
  },
};
</script>

<style scoped>
.skill-card {
  transition: transform 0.3s, background-color 0.3s;
  min-height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.skill-card:hover {
  transform: scale(1.05);
  background-color: #333;
  color: #fff;
}

.v-icon,
.font-weight-medium,
.boxicon-size {
  color: inherit;
}

.boxicon-size {
  font-size: 80px;
  margin-bottom: 16px;
}

.v-row {
  margin-left: -8px;
  margin-right: -8px;
}

.v-col {
  padding-left: 8px;
  padding-right: 8px;
}

@media (min-width: 1600px) {
  .v-col {
    flex: 0 0 16.6667%;
    max-width: 16.6667%;
  }
}
</style>

