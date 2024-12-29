<template>
  <v-container fluid class="my-10 timeline">
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
        <v-card class="education-card">
          <v-img :src="experience.image" class="education-card-image" cover></v-img>
          <v-row class="align-start px-4 pt-4">
            <v-col cols="12">
              <div class="education-school-name">{{ experience.title }}</div>
              <div class="education-major-title mt-2">{{ experience.company }}</div>
              <div class="education-location mt-2">{{ experience.location }}</div>
              <div class="education-date mt-2">{{ experience.date }}</div>
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
          image: Dental,
        },
        {
          title: "Undergraduate Research Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          date: "Aug 2024 - Present",
          image: Research,
        },
        {
          title: "Undergraduate Teaching Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          date: "Aug 2024 - Present",
          image: Teaching,
        },
        {
          title: "Software Engineer Intern",
          company: "Site Service Software Inc",
          date: "Aug 2024 - Dec 2024",
          image: Internship1,
        },
        {
          title: "Software Engineer Intern",
          company: "Hungie",
          date: "May 2024 - Aug 2024",
          image: Hungie,
        },
        {
          title: "Director of Procurement",
          company: "Undergraduate Student Association - UB",
          date: "May 2024 - Aug 2024",
          image: SA,
        },
        {
          title: "Cybersecurity Analyst",
          company: "Technical Consulting & Research Inc",
          date: "March 2024 - May 2024",
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
.education-card {
  position: relative;
  background-color: #fff;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  border-radius: 12px;
  text-align: center;
  margin-top: 40px;
}
.education-card-image {
  height: 150px;
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
}
.education-school-name {
  font-size: 20px;
  font-weight: 700;
}
.education-major-title {
  font-size: 16px;
  font-weight: 500;
}
.education-location,
.education-date {
  font-size: 14px;
  color: #757575;
}
@media (max-width: 960px) {
  .timeline-item {
    width: 100%;
    float: none;
    clear: both;
    text-align: left;
  }
  .timeline-wrapper::before {
    left: 20px;
    transform: none;
  }
  .timeline-badge {
    left: 20px;
    transform: none;
  }
}
</style>
