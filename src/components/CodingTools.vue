<template>
  <v-container class="text-center my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Tools</span>
    </h2>
    <v-btn @click="toggleTools" class="mb-4">
      {{ showTools ? 'Hide Tools' : 'Show Tools' }}
    </v-btn>
    <div v-if="showTools">
      <v-row justify="space-between" align="center">
        <v-col
            v-for="(tool, index) in tools"
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
            <template v-if="isMdiIcon(tool.icon)">
              <v-icon :size="80" class="mb-2" :style="{ color: tool.color }">
                {{ tool.icon }}
              </v-icon>
            </template>
            <template v-else>
              <i :class="[tool.icon, 'boxicon-size']" :style="{ color: tool.color }"></i>
            </template>
            <span class="font-weight-medium">{{ tool.name }}</span>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
export default {
  name: 'CodingTools',
  data() {
    return {
      showTools: false,
      tools: [
        { name: 'Visual Studio Code', icon: 'mdi-microsoft-visual-studio-code', color: '#007ACC' },
        { name: 'GitHub', icon: 'mdi-github', color: '#181717' },
        { name: 'GitLab', icon: 'bx bx-gitlab', color: '#181717' },
        { name: 'Docker', icon: 'mdi-docker', color: '#2496ED' },
        { name: 'Atlassian Jira', icon: 'mdi-jira', color: '#0052CC' },
        { name: 'Atlassian Trello', icon: 'mdi-trello', color: '#0052CC' },
      ],
    };
  },
  methods: {
    toggleTools() {
      this.showTools = !this.showTools;
    },
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
</style>
