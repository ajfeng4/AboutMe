<template>
  <v-container>
    <div id="about">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="6">
          <v-card flat>
            <h1 class="display-2 font-weight-bold mb-3">Hello, I'm Alex Feng</h1>
            <h2 class="headline font-weight-bold">Software Engineer</h2>
            <h3 class="subheading font-weight-bold mb-3">Brooklyn, New York</h3>
            <p class="body-1 mb-4">
              A full-time student taking a full course load and working 40 hours a week. Passionate about front-end and mobile development,
              with experience in technical and non-technical environments. An experienced team player and seasoned leader.
            </p>
            <SocialMedia />
          </v-card>
        </v-col>

        <v-col cols="12" md="6" class="text-center">
          <v-card flat>
            <v-icon size="150" color="grey">mdi-account-circle</v-icon>
          </v-card>
        </v-col>
      </v-row>
    </div>

    <v-row>
      <v-col cols="12">
        <v-spacer class="custom-spacer"></v-spacer>
      </v-col>
    </v-row>

    <div id="skills">
      <CodingSkills />
    </div>

    <div id="education">
      <v-row class="my-12">
        <v-col cols="12">
          <Education />
        </v-col>
      </v-row>
    </div>

    <div id="experience">
      <v-row class="my-12">
        <v-col cols="12">
          <WorkExperience />
        </v-col>
      </v-row>
    </div>

    <div id="projects">
      <v-row class="my-12">
        <v-col cols="12">
          <Projects />
        </v-col>
      </v-row>
    </div>

    <v-row class="my-12">
      <v-col cols="12">
        <GitHubStats />
      </v-col>
    </v-row>

    <div id="contact">
      <ContactMe />
    </div>
  </v-container>
</template>

<script>
import SocialMedia from '../components/SocialMedia.vue';
import CodingSkills from '../components/CodingSkills.vue';
import WorkExperience from '../components/WorkExperience.vue';
import Education from '../components/Education.vue';
import Projects from '../components/Projects.vue';
import GitHubStats from '../components/GitHubStats.vue';
import ContactMe from '../components/ContactMe.vue';

export default {
  name: 'MainPage',
  components: {
    SocialMedia,
    CodingSkills,
    WorkExperience,
    Education,
    Projects,
    GitHubStats,
    ContactMe,
  },
};
</script>

<style scoped>
.custom-spacer {
  height: 350px;
}

.v-row.my-12 {
  margin-top: 3rem;
  margin-bottom: 3rem;
}
</style>