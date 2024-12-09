<template>
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Experience</span>
    </h2>
    <div class="scrollable-experience">
      <v-row justify="center">
        <v-col cols="12" md="10">
          <v-card
              v-for="(experience, index) in experiences"
              :key="index"
              class="experience-card my-5"
              outlined
          >
            <v-row class="align-start">
              <v-col cols="2" class="text-left">
                <v-img :src="experience.image" max-width="200"></v-img>
              </v-col>
              <v-col cols="10" class="text-left">
                <div class="d-flex justify-space-between align-start">
                  <div class="experience-details">
                    <h3 class="experience-title ml-2">
                      {{ experience.title }}
                    </h3>
                    <span class="experience-company">
                      {{ experience.company }}
                    </span>
                  </div>
                  <div class="experience-date">
                    {{ experience.date }}
                  </div>
                </div>
                <div class="d-flex align-center mt-2">
                  <v-icon
                      color="grey darken-1"
                      size="20"
                      class="mr-1"
                  >mdi-map-marker</v-icon>
                  <span class="experience-location">
                    {{ experience.location }}
                  </span>
                </div>
                <div class="experience-description mt-3">
                  <p v-for="(item, idx) in experience.description" :key="idx">{{ item }}</p>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </div>
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
          company:
              "University at Buffalo School of Engineering and Applied Sciences",
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
          company:
              "University at Buffalo School of Engineering and Applied Sciences",
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
.display-2 {
  color: #333;
}
.font-weight-bold {
  font-weight: 700;
}
.experience-card {
  padding: 24px;
  background-color: #fff;
  width: 120%;
  margin-left: -50px;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 12px;
  text-align: left;
}
.experience-title {
  font-weight: 500;
  font-size: 12px;
  margin-bottom: 8px;
  word-wrap: break-word;
}
.experience-company {
  display: block;
  font-size: 12px;
  color: #757575;
  margin-top: 4px;
  word-wrap: break-word;
}
.experience-location,
.experience-date {
  font-size: 12px;
  color: #757575;
  white-space: nowrap;
}
.experience-date {
  flex-shrink: 0;
  margin-left: 8px;
}
.experience-description {
  font-size: 12px;
  color: #424242;
  margin-top: 8px;
  word-wrap: break-word;
}
.experience-details {
  flex: 1;
  min-width: 0;
  text-align: left;
}
.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
.v-img {
  margin-right: auto;
}
.scrollable-experience {
  max-height: 420px;
  overflow-y: auto;
  overflow-x: hidden;
}
/* Scrollbar Styles */
.scrollable-experience::-webkit-scrollbar {
  width: 8px;
}
.scrollable-experience::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 4px;
}
.scrollable-experience::-webkit-scrollbar-thumb {
  background: #c1c1c1;
  border-radius: 4px;
}
.scrollable-experience::-webkit-scrollbar-thumb:hover {
  background: #a8a8a8;
}
.scrollable-experience {
  scrollbar-width: thin;
  scrollbar-color: #c1c1c1 #f1f1f1;
}
</style>