<template>
  <v-container class="text-center my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Skills</span>
    </h2>
    <v-row justify="center" align="center">
      <v-col
          v-for="(skill, index) in skills"
          :key="index"
          cols="4"
          sm="3"
          md="2"
          class="d-flex justify-center align-center"
      >
        <div
            class="skill-card"
            @mouseover="hoverSkill = index"
            @mouseleave="hoverSkill = null"
        >
          <template v-if="isMdiIcon(skill.icon)">
            <v-icon
                :size="60"
                class="mb-2"
                :style="{ color: hoverSkill === index ? skill.color : '#b0b0b0' }"
            >
              {{ skill.icon }}
            </v-icon>
          </template>
          <template v-else>
            <i
                :class="[skill.icon, 'boxicon-size']"
                :style="{ color: hoverSkill === index ? skill.color : '#b0b0b0' }"
            ></i>
          </template>
          <span
              class="skill-name"
              :style="{ color: hoverSkill === index ? '#000' : '#b0b0b0' }"
          >
            {{ skill.name }}
          </span>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "CodingSkills",
  data() {
    return {
      hoverSkill: null,
      skills: [
        { name: "TypeScript", icon: "mdi-language-typescript", color: "#007acc" },
        { name: "JavaScript", icon: "mdi-language-javascript", color: "#f0db4f" },
        { name: "CSS", icon: "bx bxl-css3", color: "#264de4" },
        { name: "HTML", icon: "bx bxl-html5", color: "#e34c26" },
        { name: "React.js", icon: "mdi-react", color: "#61dafb" },
        { name: "React Native", icon: "mdi-react", color: "#61dafb" },
        { name: "Vue.js", icon: "mdi-vuejs", color: "#42b883" },
        { name: "Angular", icon: "bx bxl-angular", color: "#dd0031" },
        { name: "Node.js", icon: "mdi-nodejs", color: "#43853d" },
        { name: "Python", icon: "bx bxl-python", color: "#3776ab" },
        { name: "Java", icon: "bx bxl-java", color: "#007396" },
        { name: "C++", icon: "bx bxl-c-plus-plus", color: "#00599c" },
        { name: "Spring Boot", icon: "bx bxl-spring-boot", color: "#6db33f" },
        { name: "SQL", icon: "bx bxs-data", color: "#e38c00" },
        { name: "PostgreSQL", icon: "bx bxl-postgresql", color: "#336791" },
        { name: "Firebase", icon: "bx bxl-firebase", color: "#ffca28" },
        { name: "Supabase", icon: "bx bxl-supabase", color: "#3ecf8e" },
        { name: "Git", icon: "mdi-git", color: "#f34f29" },
      ],
    };
  },
  methods: {
    isMdiIcon(icon) {
      return icon.startsWith("mdi-");
    },
  },
};
</script>

<style scoped>
.skill-card {
  text-align: center;
  padding: 16px;
  transition: transform 0.3s;
}

.skill-card:hover {
  transform: scale(1.05);
}

.skill-name {
  display: block;
  margin-top: 8px;
  font-weight: 600;
  font-size: 14px;
}

.boxicon-size {
  font-size: 60px;
  margin-bottom: 12px;
}
</style>
