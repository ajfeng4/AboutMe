<template>
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Experience</span>
    </h2>
    <v-row>
      <v-col
          cols="12"
          md="6"
          v-for="(experience, index) in experiences"
          :key="index"
      >
        <v-card class="education-card my-10">
          <div class="education-header"></div>
          <v-row class="align-start">
            <v-col cols="2" class="text-left logo-col">
              <v-img :src="experience.image" class="education-logo"></v-img>
            </v-col>
            <v-col cols="10" class="text-left">
              <div class="education-school-name">{{ experience.title }}</div>
              <div class="education-major-title">{{ experience.company }}</div>
              <div class="education-date">{{ experience.date }}</div>
              <div class="education-location d-flex align-center mt-2">
                <v-icon color="grey darken-1" size="20" class="mr-1">mdi-map-marker</v-icon>
                {{ experience.location }}
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
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
          location: "Buffalo, New York",
          date: "Sep 2024 - Present",
          image: Dental,
        },
        {
          title: "Undergraduate Research Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          location: "Buffalo, New York",
          date: "Aug 2024 - Present",
          image: Research,
        },
        {
          title: "Undergraduate Teaching Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          location: "Buffalo, New York",
          date: "Aug 2024 - Present",
          image: Teaching,
        },
        {
          title: "Software Engineer Intern",
          company: "Site Service Software Inc",
          location: "Jamison, Pennsylvania",
          date: "Aug 2024 - Present",
          image: Internship1,
        },
        {
          title: "Software Engineer Intern",
          company: "Hungie",
          location: "Queens, New York",
          date: "May 2024 - Aug 2024",
          image: Hungie,
        },
        {
          title: "Director of Procurement",
          company: "Undergraduate Student Association - UB",
          location: "Buffalo, New York",
          date: "May 2024 - Aug 2024",
          image: SA,
        },
        {
          title: "Cybersecurity Analyst",
          company: "Technical Consulting & Research Inc",
          location: "Weston, Connecticut",
          date: "March 2024 - May 2024",
          image: cybersecurity,
        },
      ],
    };
  },
};
</script>

<style scoped>
.education-card {
  position: relative;
  padding: 60px 0 20px;
  background-color: #fff;
  border-bottom: 1px solid #e0e0e0;
  box-shadow: none;
  border-radius: 0;
  text-align: left;
}
.education-header {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 60px;
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
  margin-top: -30px;
  margin-left: 10px;
}
.education-logo {
  border-radius: 50%;
  border: 1px solid #fff;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
  object-fit: cover;
}
.education-school-name,
.education-major-title,
.education-date,
.education-location {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  display: block;
}
.education-school-name {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 12px;
  max-width: 100%;
}
.education-major-title {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 12px;
  max-width: 100%;
}
.education-date,
.education-location {
  font-size: 14px;
  color: #757575;
  max-width: 100%;
}
.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
