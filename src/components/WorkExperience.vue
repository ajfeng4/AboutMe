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
              <v-img :src="experience.image" max-width="80" class="education-logo"></v-img>
            </v-col>
            <v-col cols="10" class="text-left">
              <div class="education-school-name">{{ experience.title }}</div>
              <div class="education-major-title">{{ experience.company }}</div>
              <div class="education-date">{{ experience.date }}</div>
              <div class="education-location d-flex align-center mt-2">
                <v-icon color="grey darken-1" size="20" class="mr-1">mdi-map-marker</v-icon>
                {{ experience.location }}
              </div>
              <div class="education-description mt-3">
                <p v-for="(item, idx) in experience.description" :key="idx">{{ item }}</p>
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
          description: [
            "Modernized and refined the School of Dental Medicine (SDM) website to streamline the application process for prospective applicants.",
            "Identified and fixed inconsistencies and bugs on the SDM website; recommended and implemented enhancements to improve user experience.",
            "Collaborated closely with SDM admissions, conducting regular meetings and interviews with students to gather critical feedback for website improvements.",
          ],
          type: "Part-Time",
          image: Dental,
        },
        {
          title: "Undergraduate Research Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          location: "Buffalo, New York",
          date: "Aug 2024 - Present",
          description: [
            "Developed a React Native mobile application for Professor Wenyao Xu Drink Intake Project to monitor users drinking habits based on detected drinking sounds.",
            "Composed research proposals and delivered weekly reports during stand-up meetings with Professor Xu.",
            "Utilized React Native Framework, React Native Paper, TypeScript, and Tailwind CSS for front-end development.",
            "Implemented Python and Flask for the back end, integrating AWS for database management.",
            "Designed and presented UI/UX prototypes using Figma to professors, Ph.D. researchers, and potential users.",
            "Integrated Software Development Life Cycle (SDLC) processes and managed tasks using Kanban boards like Trello and Jira.",
          ],
          type: "Part-Time",
          image: Research,
        },
        {
          title: "Undergraduate Teaching Assistant",
          company: "University at Buffalo School of Engineering and Applied Sciences",
          location: "Buffalo, New York",
          date: "Aug 2024 - Present",
          description: [
            "Assisted the professor in teaching CSE410: 3D Game Development using C++ and Unreal Engine to over 100 students.",
            "Held weekly office hours to provide guidance and support to students.",
            "Led and mentored groups of students in developing games, fostering collaboration and technical skills.",
            "Graded weekly assignments and provided constructive feedback.",
            "Responded to student inquiries and facilitated discussions through Piazza.",
            "Supported students in learning and applying C++ and Unreal Engine for game development projects",
          ],
          type: "Internship",
          image: Teaching,
        },
        {
          title: "Software Engineer Intern",
          company: "Site Service Software Inc",
          location: "Jamison, Pennsylvania",
          date: "Aug 2024 - Present",
          description: [
            "Migrated legacy systems to Java and Spring Boot, increasing efficiency by 35% and reducing maintenance costs.",
            "Updated the front end of legacy software using JavaScript and Tailwind CSS, reducing technical debt.",
            "Utilized Azure SQL to build and connect user databases.",
            "Collaborated with cross-functional teams using Git to ensure successful integration and maintain clean code.",
            "Participated in weekly stand-up meetings and full software development cycles, adhering to Agile methodologies.",
          ],
          type: "Internship",
          image: Internship1,
        },
        {
          title: "Software Engineer Intern",
          company: "Hungie",
          location: "Queens, New York",
          date: "May 2024 - Aug 2024",
          description: [
            "Developed a mobile iOS/Android app powered by AI to recommend and cater food based on users taste preferences.",
            "Implemented scalable full-stack features using TypeScript, React Native, Python, and Firebase.",
            "Reduced technical debt by 50% through the use of Tailwind CSS and API optimizations, improving load times by 20%.",
            "Integrated alternative APIs and services such as SendGrid, Twilio, and Swagger, reducing costs significantly and overhauled deprecated systems.",
            "Collaborated with cross-functional teams using tools like Notion, Trello, Jira, and Figma for work-flow management and front-end development.",
          ],
          type: "Internship",
          image: Hungie,
        },
        {
          title: "Director of Procurement",
          company: "Undergraduate Student Association - UB",
          location: "Buffalo, New York",
          date: "May 2024 - Aug 2024",
          description: [
            "Negotiated competitive rates with vendors, saving student clubs significantly annually.",
            "Managed a large number of weekly purchase orders, maintaining transparency and accuracy.",
            "Led a team of 5 Procurement Assistants, refining procurement processes to better serve undergraduate clubs.",
          ],
          type: "Internship",
          image: SA,
        },
        {
          title: "Cybersecurity Analyst",
          company: "Technical Consulting & Research Inc",
          location: "Weston, Connecticut",
          date: "March 2024 - May 2024",
          description: [
            "Researched NIST compliance and conducted weekly presentations/seminars about NIST compliance and best security practices.",
            "Ran demos involving PowerShell and Linux to demonstrate practical applications.",
            "Worked regularly with Microsoft 365 applications such as Microsoft Purview.",
          ],
          type: "Internship",
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
}

.education-school-name {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 12px;
  word-wrap: break-word;
}

.education-major-title {
  font-size: 18px;
  font-weight: 500;
  margin-bottom: 12px;
  word-wrap: break-word;
}

.education-date,
.education-location {
  font-size: 14px;
  color: #757575;
}

.education-description {
  font-size: 14px;
  color: #424242;
  margin-top: 16px;
  word-wrap: break-word;
}

.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
