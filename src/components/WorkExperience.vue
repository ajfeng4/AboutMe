<template>
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Experience</span>
    </h2>
    <v-timeline>
      <v-timeline-item
          v-for="(experience, index) in experiences"
          :key="index"
          :color="index % 2 === 0 ? 'primary' : 'secondary'"
          :right="index % 2 !== 0"
          :left="index % 2 === 0"
      >
        <template #icon>
          <v-img :src="experience.image" class="timeline-logo"></v-img>
        </template>
        <v-card
            class="experience-card my-10"
        >
          <div class="experience-header"></div>
          <v-row class="align-start">
            <v-col cols="2" class="text-left logo-col">
              <v-img :src="experience.image" max-width="120" class="experience-logo"></v-img>
            </v-col>
            <v-col cols="10" class="text-left">
              <div class="experience-title">{{ experience.title }}</div>
              <div class="experience-company">{{ experience.company }}</div>
              <div class="experience-date">{{ experience.date }}</div>
              <div class="experience-location d-flex align-center mt-2">
                <v-icon color="grey darken-1" size="20" class="mr-1">mdi-map-marker</v-icon>
                {{ experience.location }}
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
import Dental from "@/assets/dental.png";
import Research from "@/assets/davis.png";
import Teaching from "@/assets/davis.png";
import Internship1 from "@/assets/service.png";
import Hungie from "@/assets/hungie.png";
import SA from "@/assets/sa.png";
import cybersecurity from "@/assets/tcr.png";

export default {
  name: "WorkExperience",
  data() {
    return {
      experiences: [
        {
          title: "Web Development Assistant",
          company: "University at Buffalo School of Dental Medicine",
          date: "Sep 2024 - Present",
          location: "Buffalo, New York",
          image: Dental,
        },
        {
          title: "Undergraduate Research Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          date: "Aug 2024 - Present",
          location: "Buffalo, New York",
          image: Research,
        },
        {
          title: "Undergraduate Teaching Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          date: "Aug 2024 - Present",
          location: "Buffalo, New York",
          image: Teaching,
        },
        {
          title: "Software Engineer Intern",
          company: "Site Service Software Inc",
          date: "Aug 2024 - Dec 2024",
          location: "Jamison, Pennslyvania",
          image: Internship1,
        },
        {
          title: "Software Engineer Intern",
          company: "Hungie",
          date: "May 2024 - Aug 2024",
          location: "New York City, New York",
          image: Hungie,
        },
        {
          title: "Director of Procurement",
          company: "Undergraduate Student Association - UB",
          date: "May 2024 - Aug 2024",
          location: "Buffalo, New York",
          image: SA,
        },
        {
          title: "Cybersecurity Analyst",
          company: "Technical Consulting & Research Inc",
          date: "March 2024 - May 2024",
          location: "Weston, Connecticut",
          image: cybersecurity,
        },
      ],
    };
  },
};
</script>

<style scoped>
.timeline {
  position: relative;
  padding: 0;
}
.timeline-wrapper {
  position: relative;
}
.timeline-wrapper::before {
  content: "";
  position: absolute;
  left: 50%;
  top: 0;
  width: 4px;
  background: #333;
  height: 100%;
  transform: translateX(-50%);
}
.timeline-item {
  width: 40%;
  padding: 20px;
  box-sizing: border-box;
  position: relative;
}
.timeline-item.left {
  float: left;
  text-align: right;
}
.timeline-item.right {
  float: right;
  text-align: left;
}
.timeline-badge {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  background: #fff;
  border: 4px solid #fff;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}
.timeline-logo {
  border-radius: 50%;
  object-fit: cover;
  width: 48px;
  height: 48px;
}
.experience-card {
  position: relative;
  padding: 120px 0 40px;
  background-color: #fff;
  border-bottom: 1px solid #e0e0e0;
  box-shadow: none;
  border-radius: 0;
  text-align: left;
}

.experience-header {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 120px;
  background: url('../assets/campus.png') center center/cover no-repeat;
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
}

.logo-col {
  position: relative;
  z-index: 1;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  margin-top: -60px;
  margin-left: 10px;
}

.experience-logo {
  border-radius: 50%;
  border: 1px solid #fff;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
}

.experience-title {
  font-size: 28px;
  font-weight: 700;
  margin-bottom: 12px;
  word-wrap: break-word;
}

.experience-company {
  font-size: 20px;
  font-weight: 500;
  margin-bottom: 12px;
  word-wrap: break-word;
}

.experience-date,
.experience-location {
  font-size: 16px;
  color: #757575;
}

.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
