<template>
  <v-container>
    <v-row align="center" justify="center" class="my-10">
      <v-col cols="12" md="12">
        <v-card flat>
          <h1 class="display-2 font-weight-bold mb-5">My Experience</h1>

          <v-card
              v-for="(experience, index) in experiences"
              :key="index"
              outlined
              elevation="2"
              class="experience-card mb-5 py-4 px-6"
          >
            <v-row>
              <v-col cols="3" class="d-flex align-center justify-center">
                <div class="image-container">
                  <v-img :src="experience.image" contain></v-img>
                </div>
              </v-col>
              <v-col cols="9">
                <v-row>
                  <v-col cols="8" class="d-flex align-center">
                    <h3 class="font-weight-bold">
                      {{ experience.title }}
                    </h3>
                    <v-chip
                        v-if="experience.type"
                        class="ml-3"
                        color="blue lighten-4"
                        text-color="blue darken-2"
                        small
                    >
                      {{ experience.type }}
                    </v-chip>
                  </v-col>
                </v-row>

                <v-row align="center" class="mt-2">
                  <v-col cols="4" class="d-flex align-center">
                    <v-icon color="grey darken-1" size="20" class="mr-2"
                    >mdi-office-building</v-icon
                    >
                    <span>{{ experience.company }}</span>
                  </v-col>
                  <v-col cols="4" class="d-flex align-center">
                    <v-icon color="grey darken-1" size="20" class="mr-2"
                    >mdi-map-marker</v-icon
                    >
                    <span>{{ experience.location }}</span>
                  </v-col>
                  <v-col cols="4" class="d-flex align-center justify-end">
                    <v-icon color="grey darken-1" size="20" class="mr-2"
                    >mdi-calendar</v-icon
                    >
                    <span>{{ experience.date }}</span>
                  </v-col>
                </v-row>

                <v-list class="mt-3">
                  <v-list-item
                      v-for="(item, idx) in experience.description"
                      :key="idx"
                      class="bullet-point"
                  >
                    <v-card class="bullet-card pa-3 mb-3">
                      <v-row align="center">
                        <v-icon color="primary" class="mr-2"
                        >mdi-checkbox-marked-circle-outline</v-icon
                        >
                        <span>{{ item }}</span>
                      </v-row>
                    </v-card>
                  </v-list-item>
                </v-list>
              </v-col>
            </v-row>
          </v-card>
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
.display-2 {
  color: #333;
}
.font-weight-bold {
  font-weight: 700;
}
.experience-card {
  background-color: #f9f9f9;
  border-radius: 12px;
  width: 100%;
}
.v-icon,
.font-weight-medium,
.text--secondary {
  color: inherit;
}
.bullet-card {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
.image-container {
  width: 150px;
  height: 150px;
  border-radius: 12px;
  overflow: hidden;
  background-color: #fff;
}
.image-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
