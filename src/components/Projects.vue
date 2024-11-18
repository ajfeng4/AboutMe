<script setup>
import { Icon } from '@iconify/vue';
import ProjectLinkButton from './ProjectLinkButton.vue';

const projects = [
  {
    year: "Fall 2024",
    title: "Drink Intake App",
    description: "React Native IOS/Andriod App to keep track of user's hydration levels. The app helps build and recommend hydration goals and plans to help users meet their daily hydration needs and maintain a more healthier life-style and habits",
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
      { icon: "simple-icons:postgresql", name: "Postgresql", color: "#4169E1" },
      { icon: "simple-icons:expo", name: "Expo Go", color: "#000020" },
      { icon: "simple-icons:reactrouter", name: "React Router", color: "#CA4245" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Find a Mechanic",
    description: "React Native IOS/Andriod App to connect customers to local mechanics in their area. Part of CSE302's Experential Learning and Research course",
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
    description: "Invovled in building an AI powered food buddy built to recommend and cater meals to meet the specific taste buds and preferences of users. Utilizing comprehensive alogrithms and machine learning models to serve up specific recommendations to meet the user's pallete. Developed front-end with clean and efficent user interfaces using Typescript,React Native and Tailwind CSS. Processed and managed backend with user perferences using Python and Flask. Ran the mobile IOS/Andriod environment using Expo Go. Managed and built the app's database and authentication using Firebase, Google Cloud and Sendgrid",
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
    description: "Responsive social media application that gives users the full power to shape their social media landscape. Utilized JavaScript,Typescript,CSS and HTML to build a clean and responsive front-end. Dystopia is available not only through the web but also available and compatible on mobile. Utilized Swagger API to manage the backend database and to fetch and modify user attributes. Collaborated closely with a team of four software engineers to meet weekly objectives and maintain a strict and effective Agile enivronment meeting the requirements set by the Project Manager",
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
    description: "Inventory Manager is a mobile friendly website built to keep track of a user's pantry and their storage",
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
      { icon: "simple-icons:mui", name: "MaterialUI", color: "#007FFF" },
      { icon: "simple-icons:nextdotjs", name: "Next.js", color: "#000000" },
      { icon: "simple-icons:vercel", name: "Vercel", color: "#000000" },
    ],
  },
  {
    year: "Fall 2024",
    title: "Brighterspace",
    description: "An interactive educational platform bridging the disconnect between learning and teaching. Utilized JavaScript,Typescript,React.js for front-end developement to build clean and scalabe screens and pages. Utilized PHP to manage the back-end database, to fetch and modify student data and retreive and display user atrributes. Utilized Apache to host the platform. Worked in an agile environment and meet weekly sprints and objectives set by the project manager",
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
  <v-container>
    <h1 class="title">Coding Projects</h1>
    <v-row>
      <v-col
          v-for="(project, index) in projects"
          :key="index"
          cols="12"
          sm="6"
          md="4"
      >
        <v-card class="project-card" outlined>
          <v-card-header class="project-header">
            <Icon :icon="project.icon" class="project-icon" />
            <div class="project-title-container">
              <h2 class="project-title">{{ project.title }}</h2>
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
          </v-card-header>
          <v-card-text>
            <p class="project-year">{{ project.year }}</p>
            <p class="project-description">{{ project.description }}</p>
            <div class="project-tags">
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
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

.project-card {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.project-header {
  display: flex;
  align-items: center;
  width: 100%;
}

.project-icon {
  font-size: 3rem;
  color: #1976d2;
  margin-right: 1rem;
}

.project-title-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
}

.project-title {
  font-size: 1.5rem;
  margin: 0;
  flex-grow: 1;
}

.project-links {
  display: flex;
  gap: 0.5rem;
  margin-left: 1rem;
}

.project-year {
  font-size: 0.9rem;
  color: #757575;
  margin-top: 0.5rem;
}

.project-description {
  margin-bottom: 1rem;
  color: #424242;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  display: flex;
  align-items: center;
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
}

.tag-icon {
  width: 20px;
  height: 20px;
  margin-right: 0.5rem;
}

.tag-text {
  font-size: 0.85rem;
  color: #fff;
}

.link-button {
  padding: 0.25rem 0.75rem;
  border-radius: 15px;
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.85rem;
}
</style>
