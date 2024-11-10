<script setup>
const projects = [
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    githubLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    websiteLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    tags: [
      { icon: "mdi-vuejs", name: "Vue.js" },
      { icon: "mdi-javascript", name: "JavaScript" },
      { icon: "mdi-database", name: "Database" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    githubLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    websiteLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    tags: [
      { icon: "mdi-vuejs", name: "Vue.js" },
      { icon: "mdi-javascript", name: "JavaScript" },
      { icon: "mdi-database", name: "Database" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    githubLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    websiteLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    tags: [
      { icon: "mdi-vuejs", name: "Vue.js" },
      { icon: "mdi-javascript", name: "JavaScript" },
      { icon: "mdi-database", name: "Database" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    githubLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    websiteLink: "https://github.com/ajfeng4/DrinkIntakeResearch",
    tags: [
      { icon: "mdi-vuejs", name: "Vue.js" },
      { icon: "mdi-javascript", name: "JavaScript" },
      { icon: "mdi-database", name: "Database" },
    ],
  },
];
</script>

<template>
  <v-container>
    <h1 class="text-center display-1 mb-8">Coding Projects</h1>
    <v-row>
      <v-col cols="12" v-for="(project, index) in projects" :key="index">
        <v-card outlined class="pa-4 mb-6">
          <v-row align="center">
            <v-col cols="2" class="text-center">
              <v-icon size="80" color="primary">{{ project.icon }}</v-icon>
            </v-col>
            <v-col cols="10">
              <div class="project-header">
                <h2 class="headline font-weight-bold">{{ project.title }}</h2>
                <v-btn icon :href="project.githubLink" target="_blank">
                  <v-icon>mdi-github</v-icon>
                </v-btn>
                <v-btn icon :href="project.websiteLink" target="_blank">
                  <v-icon>mdi-web</v-icon>
                </v-btn>
              </div>
              <p class="subtitle-1 text--primary font-weight-light">{{ project.year }}</p>
              <p class="body-2 mb-4">{{ project.description }}</p>
              <div class="tags">
                <div
                    v-for="(tag, tagIndex) in project.tags"
                    :key="tagIndex"
                    class="tag-container"
                >
                  <v-icon size="30" class="mr-2" color="secondary">{{ tag.icon }}</v-icon>
                  <span class="tag-text">{{ tag.name }}</span>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.display-1 {
  margin-bottom: 2rem;
}
.project-header {
  display: flex;
  align-items: center;
}
.project-header h2 {
  margin-right: 16px;
}
.tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}
.tag-container {
  display: flex;
  align-items: center;
  padding: 9px;
  border-radius: 30px;
  background-color: #f9f9f9;
  margin-left: 1px;
}
.tag-text {
  margin-left: 4px;
  font-size: 14px;
  font-weight: 500;
}
</style>

