<script setup>
import { ref } from 'vue';
import { Icon } from '@iconify/vue';
import ProjectLinkButton from './ProjectLinkButton.vue';
import Drinkintake1 from "@/assets/drinkintake3.png";
import Drinkintake2 from "@/assets/drinkintake3.png";
import FindMechanic1 from "@/assets/drinkintake3.png";
import FindMechanic2 from "@/assets/drinkintake3.png";
import Hungie1 from "@/assets/drinkintake3.png";
import Hungie2 from "@/assets/drinkintake3.png";
import Dystopia1 from "@/assets/drinkintake3.png";
import Dystopia2 from "@/assets/drinkintake3.png";
import InventoryManager1 from "@/assets/drinkintake3.png";
import InventoryManager2 from "@/assets/drinkintake3.png";
import Brighterspace1 from "@/assets/drinkintake3.png";
import Brighterspace2 from "@/assets/drinkintake3.png";

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
    images: [
      Drinkintake1,
      Drinkintake2
    ]
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
    images: [
      FindMechanic1,
      FindMechanic2
    ]
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
    images: [
      Hungie1,
      Hungie2
    ]
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
    images: [
      Dystopia1,
      Dystopia2
    ]
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
    images: [
      InventoryManager1,
      InventoryManager2
    ]
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
    images: [
      Brighterspace1,
      Brighterspace2
    ]
  },
];
</script>

<template>
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Projects</span>
    </h2>
    <v-row>
      <v-col
          cols="12"
          md="6"
          v-for="(project, index) in projects"
          :key="index"
      >
        <v-card class="project-card my-10">
          <div class="icon-circle">
            <Icon :icon="project.icon" class="icon-in-circle" />
          </div>
          <v-carousel hide-delimiter-background height="300px" class="project-carousel">
            <v-carousel-item
                v-for="(image, imgIndex) in project.images"
                :key="imgIndex"
            >
              <v-img :src="image" class="project-image" cover></v-img>
            </v-carousel-item>
          </v-carousel>
          <div class="project-content">
            <div class="project-title">
              {{ project.title }}
              <span
                  v-for="(link, linkIndex) in project.links"
                  :key="linkIndex"
              >
                <ProjectLinkButton
                    :icon="link.icon"
                    :text="link.name"
                    :href="link.href"
                    :color="link.color"
                    class="link-button"
                />
              </span>
            </div>
            <div class="project-description">{{ project.description }}</div>
            <div class="project-year">{{ project.year }}</div>
            <div class="d-flex align-center mt-2 flex-wrap">
              <span
                  v-for="(tag, tagIndex) in project.tags"
                  :key="tagIndex"
                  class="tag"
                  :style="{ backgroundColor: tag.color }"
              >
                <Icon :icon="tag.icon" class="tag-icon" />
                <span class="tag-text">{{ tag.name }}</span>
              </span>
            </div>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.project-card {
  position: relative;
  background-color: #fff;
  border: none;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  padding-bottom: 20px;
}
.icon-circle {
  position: absolute;
  top: 20px;
  left: 20px;
  background: #fff;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 2;
}
.icon-in-circle {
  font-size: 32px;
  color: #1976d2;
}
.project-carousel {
  border-radius: 0;
}
.project-image {
  border-radius: 0;
}
.project-content {
  margin-top: 20px;
  padding: 0 20px;
}
.project-title {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}
.project-description {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 12px;
}
.project-year {
  font-size: 14px;
  color: #757575;
}
.tag {
  display: flex;
  align-items: center;
  padding: 0.2rem 0.5rem;
  border-radius: 12px;
  margin: 4px;
}
.tag-icon {
  width: 16px;
  height: 16px;
  margin-right: 0.3rem;
  color: #fff;
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
  margin-left: 8px;
}
.display-2 {
  color: #333;
}
.font-weight-bold {
  font-weight: 700;
}
</style>
