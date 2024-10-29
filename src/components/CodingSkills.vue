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
          sm="4"
          md="3"
          class="d-flex justify-center"
      >
        <v-card
            outlined
            elevation="2"
            class="skill-card pa-4 d-flex flex-column align-center"
            width="100%"
        >
          <template v-if="isMdiIcon(skill.icon)">
            <v-icon :size="80" class="mb-2" :style="{ color: skill.color }">{{ skill.icon }}</v-icon>
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
        { name: 'React.js', icon: 'mdi-react', color: '#f0db4f' },
        { name: 'React Native', icon: 'mdi-react', color: '#61dafb' },
        { name: 'CSS', icon: 'bx bxl-css3', color: '#264de4' },
        { name: 'HTML', icon: 'bx bxl-html5', color: '#e34c26' },
        { name: 'Vue.js', icon: 'mdi-vuejs', color: '#42b883' },
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
  border: 1px solid #333;
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
    flex: 0 0 20%;
    max-width: 20%;
  }
}
</style>

