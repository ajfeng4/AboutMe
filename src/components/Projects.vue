<script setup>
import { Icon } from '@iconify/vue';
import ProjectLinkButton from './ProjectLinkButton.vue';

const projects = [
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    links: [
      {
        icon: "mdi-github",
        name: "GitHub",
        color: "#333",
        href: "https://github.com/ajfeng4/DrinkIntakeResearch"
      },
      {
        icon: "mdi-web",
        name: "Website",
        color: "#2196F3",
        href: "https://github.com/ajfeng4/DrinkIntakeResearch"
      }
    ],
    tags: [
      { icon: "mdi-language-typescript", name: "TypeScript", color: "#007acc" },
      { icon: "simple-icons:python", name: "Python", color: "#3776AB" },
      { icon: "mdi-react", name: "React Native", color: "#61dafb" },
      { icon: "simple-icons:supabase", name: "Supabase", color: "#3ECF8E" },
      { icon: "simple-icons:postgresql", name: "Postgresql", color: "#4169E1" },
      { icon: "simple-icons:expo", name: "Expo Go", color: "#000020" },
      { icon: "simple-icons:reactrouter", name: "React Router", color: "#CA4245" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Find a Mechanic",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    links: [
      {
        icon: "mdi-github",
        name: "GitHub",
        color: "#333",
        href: "https://github.com/ajfeng4/FindAMechanic"
      },
      {
        icon: "mdi-web",
        name: "Website",
        color: "#2196F3",
        href: "https://findamechanic.com"
      }
    ],
    tags: [
      { icon: "mdi-language-javascript", name: "JavaScript", color: "#F7DF1E" },
      { icon: "simple-icons:php", name: "PHP", color: "#777BB4" },
      { icon: "simple-icons:mysql", name: "MySQL", color: "#4479A1" },
      { icon: "mdi-react", name: "React Native", color: "#61dafb" },
      { icon: "simple-icons:expo", name: "Expo Go", color: "#000020" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Hungie Mobile App",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    links: [
      {
        icon: "mdi-github",
        name: "GitHub",
        color: "#333",
        href: "https://github.com/ajfeng4/HungieMobileApp"
      },
      {
        icon: "mdi-web",
        name: "Website",
        color: "#2196F3",
        href: "https://hungieapp.com"
      }
    ],
    tags: [
      { icon: "mdi-language-typescript", name: "TypeScript", color: "#007acc" },
      { icon: "simple-icons:python", name: "Python", color: "#3776AB" },
      { icon: "mdi-react", name: "React Native", color: "#61dafb" },
      { icon: "simple-icons:tailwindcss", name: "Tailwind CSS", color: "#06B6D4" },
      { icon: "simple-icons:nodedotjs", name: "Node.js", color: "#5FA04E" },
      { icon: "simple-icons:flask", name: "Flask", color: "#000000" },
      { icon: "simple-icons:firebase", name: "Firebase", color: "#DD2C00" },
      { icon: "simple-icons:expo", name: "Expo Go", color: "#000020" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Dystopia",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    links: [
      {
        icon: "mdi-github",
        name: "GitHub",
        color: "#333",
        href: "https://github.com/ajfeng4/Dystopia"
      },
      {
        icon: "mdi-web",
        name: "Website",
        color: "#2196F3",
        href: "https://dystopia.com"
      }
    ],
    tags: [
      { icon: "mdi-language-javascript", name: "JavaScript", color: "#F7DF1E" },
      { icon: "simple-icons:css3", name: "CSS", color: "#1572B6" },
      { icon: "simple-icons:bootstrap", name: "Bootstrap", color: "#7952B3" },
      { icon: "simple-icons:swagger", name: "Swagger", color: "#85EA2D" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Inventory Manager",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    links: [
      {
        icon: "mdi-github",
        name: "GitHub",
        color: "#333",
        href: "https://github.com/ajfeng4/InventoryManager"
      },
      {
        icon: "mdi-web",
        name: "Website",
        color: "#2196F3",
        href: "https://inventorymanager.com"
      }
    ],
    tags: [
      { icon: "mdi-language-javascript", name: "JavaScript", color: "#F7DF1E" },
      { icon: "simple-icons:css3", name: "CSS", color: "#1572B6" },
      { icon: "simple-icons:mui", name: "MaterialUI", color: "#007FFF" },
      { icon: "simple-icons:nextdotjs", name: "Next.js", color: "#000000" },
      { icon: "simple-icons:vercel", name: "Vercel", color: "#000000" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Brighterspace",
    description: "Project to keep track of user intake",
    icon: "mdi-code-tags",
    links: [
      {
        icon: "mdi-github",
        name: "GitHub",
        color: "#333",
        href: "https://github.com/ajfeng4/Brighterspace"
      },
      {
        icon: "mdi-web",
        name: "Website",
        color: "#2196F3",
        href: "https://brighterspace.com"
      }
    ],
    tags: [
      { icon: "mdi-language-javascript", name: "JavaScript", color: "#F7DF1E" },
      { icon: "simple-icons:css3", name: "CSS", color: "#1572B6" },
      { icon: "simple-icons:html5", name: "HTML", color: "#E34F26" },
      { icon: "simple-icons:php", name: "PHP", color: "#777BB4" },
      { icon: "simple-icons:mysql", name: "MySQL", color: "#4479A1" },
      { icon: "simple-icons:apache", name: "Apache", color: "#D22128" },
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
                <div class="links">
                  <ProjectLinkButton
                      v-for="(link, linkIndex) in project.links"
                      :key="linkIndex"
                      :icon="link.icon"
                      :text="link.name"
                      :href="link.href"
                      :color="link.color"
                  />
                </div>
              </div>
              <p class="subtitle-1 text--primary font-weight-light">{{ project.year }}</p>
              <p class="body-2 mb-4">{{ project.description }}</p>
              <div class="tags">
                <div
                    v-for="(tag, tagIndex) in project.tags"
                    :key="tagIndex"
                    class="tag-container"
                    :style="{ backgroundColor: tag.color }"
                >
                  <Icon :icon="tag.icon" width="30" height="30" class="mr-2" color="white" />
                  <span class="tag-text" style="color: white;">{{ tag.name }}</span>
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
.links {
  display: flex;
  align-items: center;
  gap: 8px;
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
  margin-left: 1px;
}
.tag-text {
  margin-left: 4px;
  font-size: 14px;
  font-weight: 500;
}
</style>
