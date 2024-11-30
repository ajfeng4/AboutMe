<script setup>
import { ref } from 'vue';
import { Icon } from '@iconify/vue';
import ProjectLinkButton from './ProjectLinkButton.vue';
import placeholderImage from '../assets/davis.png';

const projects = [
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "React Native iOS/Android app to track user's hydration levels. The app helps build and recommend hydration goals to help users meet their daily hydration needs and maintain a healthier lifestyle.",
    icon: "mdi-cup",
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
      { icon: "simple-icons:postgresql", name: "PostgreSQL", color: "#4169E1" },
      { icon: "simple-icons:expo", name: "Expo Go", color: "#000020" },
      { icon: "simple-icons:reactrouter", name: "React Router", color: "#CA4245" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Find a Mechanic",
    description: "React Native iOS/Android app connecting customers to local mechanics. Part of CSE302's Experiential Learning and Research course.",
    icon: "mdi-car-wrench",
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
    description: "AI-powered food buddy recommending meals based on user preferences. Developed front-end with TypeScript, React Native, and Tailwind CSS. Managed backend with Python and Flask. Ran the mobile environment using Expo Go. Managed database and authentication with Firebase and Google Cloud.",
    icon: "mdi-food",
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
    description: "Responsive social media application empowering users to shape their social media landscape. Utilized JavaScript, TypeScript, CSS, and HTML for front-end. Managed backend with Swagger API. Collaborated in an Agile environment with a team of four software engineers.",
    icon: "mdi-fire-circle",
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
    description: "Mobile-friendly website to track user's pantry and storage.",
    icon: "mdi-cart",
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
        href: ""
      }
    ],
    tags: [
      { icon: "mdi-language-javascript", name: "JavaScript", color: "#F7DF1E" },
      { icon: "simple-icons:css3", name: "CSS", color: "#1572B6" },
      { icon: "simple-icons:mui", name: "Material UI", color: "#007FFF" },
      { icon: "simple-icons:nextdotjs", name: "Next.js", color: "#000000" },
      { icon: "simple-icons:vercel", name: "Vercel", color: "#000000" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Brighterspace",
    description: "Interactive educational platform bridging the gap between learning and teaching. Used JavaScript, TypeScript, React.js for front-end. Managed backend with PHP and MySQL. Hosted the platform on Apache. Worked in an Agile environment to meet weekly sprints.",
    icon: "mdi-school",
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
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Projects</span>
    </h2>
    <div class="scrollable-projects">
      <v-row justify="center">
        <v-col cols="12" md="10">
          <v-card
              v-for="(project, index) in projects"
              :key="index"
              class="project-card my-5"
              outlined
          >
            <v-row class="align-start">
              <v-col cols="2" class="text-left">
                <Icon :icon="project.icon" class="project-icon" />
              </v-col>
              <v-col cols="10" class="text-left">
                <div class="d-flex justify-space-between align-start">
                  <div class="project-details">
                    <h3 class="project-title">
                      {{ project.title }}
                    </h3>
                    <div class="project-links">
                      <ProjectLinkButton
                          v-for="(link, linkIndex) in project.links"
                          :key="linkIndex"
                          :icon="link.icon"
                          :text="link.name"
                          :href="link.href"
                          :color="link.color"
                          class="link-button"
                      />
                    </div>
                  </div>
                  <div class="project-year">
                    {{ project.year }}
                  </div>
                </div>
                <div class="project-description mt-3">
                  <p>{{ project.description }}</p>
                </div>
                <div class="project-tags mt-2">
                  <div
                      v-for="(tag, tagIndex) in project.tags"
                      :key="tagIndex"
                      class="tag"
                      :style="{ backgroundColor: tag.color }"
                  >
                    <Icon :icon="tag.icon" class="tag-icon" />
                    <span class="tag-text">{{ tag.name }}</span>
                  </div>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<style scoped>
.display-2 {
  color: #333;
}
.font-weight-bold {
  font-weight: 700;
}
.project-card {
  padding: 24px;
  background-color: #fff;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 12px;
  text-align: left;
}
.project-icon {
  font-size: 2rem;
  color: #1976d2;
}
.project-details {
  flex: 1;
  min-width: 0;
}
.project-title {
  font-weight: 500;
  font-size: 1.2rem;
  margin-bottom: 8px;
}
.project-links {
  display: flex;
  gap: 0.5rem;
}
.project-year {
  font-size: 0.9rem;
  color: #757575;
  white-space: nowrap;
}
.project-description {
  font-size: 0.9rem;
  color: #424242;
}
.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.25rem;
}
.tag {
  display: flex;
  align-items: center;
  padding: 0.2rem 0.5rem;
  border-radius: 12px;
}
.tag-icon {
  width: 16px;
  height: 16px;
  margin-right: 0.3rem;
}
.tag-text {
  font-size: 0.75rem;
  color: #fff;
}
.link-button {
  padding: 0.2rem 0.5rem;
  border-radius: 12px;
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 0.3rem;
  font-size: 0.75rem;
}
.scrollable-projects {
  max-height: 420px;
  overflow-y: auto;
  overflow-x: hidden;
}
/* Scrollbar Styles */
.scrollable-projects::-webkit-scrollbar {
  width: 8px;
}
.scrollable-projects::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 4px;
}
.scrollable-projects::-webkit-scrollbar-thumb {
  background: #c1c1c1;
  border-radius: 4px;
}
.scrollable-projects::-webkit-scrollbar-thumb:hover {
  background: #a8a8a8;
}
</style>
