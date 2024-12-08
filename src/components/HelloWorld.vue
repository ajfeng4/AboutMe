<template>
  <div style="width:100%;margin:0;padding:0;">
    <div id="about" class="section">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="6">
          <Landing />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <ProfilePic />
        </v-col>
      </v-row>
    </div>

    <div id="landing-section" class="section">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="6">
          <AboutMe />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <LandingPic />
        </v-col>
      </v-row>
    </div>

    <div id="skills-section" class="section">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="8" class="text-center">
          <CodingSkills />
        </v-col>
      </v-row>
    </div>

    <div id="spacer-section" class="section">
      <v-row align="center" justify="center">
        <v-col cols="12">
          <v-spacer class="custom-spacer"></v-spacer>
        </v-col>
      </v-row>
    </div>

    <div id="tools" class="section">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="8">
          <CodingTools />
        </v-col>
      </v-row>
    </div>

    <div id="education" class="section">
      <v-row align="center" justify="center" class="my-12">
        <v-col cols="12" md="8" class="text-center">
          <Education />
        </v-col>
      </v-row>
    </div>

    <div id="experience" class="section">
      <v-row align="center" justify="center" class="my-12">
        <v-col cols="12" md="8" class="text-center">
          <WorkExperience />
        </v-col>
      </v-row>
    </div>

    <div id="projects" class="section">
      <v-row align="center" justify="center" class="my-12">
        <v-col cols="12" md="8" class="text-center">
          <Projects />
        </v-col>
      </v-row>
    </div>

    <div id="github-stats" class="section">
      <v-row align="center" justify="center" class="my-12">
        <v-col cols="12" md="8" class="text-center">
          <GitHubStats />
        </v-col>
      </v-row>
    </div>

    <div id="contact" class="section">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="8" class="text-center">
          <ContactMe />
        </v-col>
      </v-row>
    </div>

    <Footer />
  </div>
</template>

<script>
import Landing from '../components/Landing.vue';
import SocialMedia from '../components/SocialMedia.vue';
import CodingSkills from '../components/CodingSkills.vue';
import CodingTools from '../components/CodingTools.vue';
import WorkExperience from '../components/WorkExperience.vue';
import Education from '../components/Education.vue';
import Projects from '../components/Projects.vue';
import GitHubStats from '../components/GitHubStats.vue';
import ContactMe from '../components/ContactMe.vue';
import Footer from '../components/Footer.vue';
import AboutMe from '../components/AboutMe.vue';
import ProfilePic from '../components/ProfilePic.vue';
import LandingPic from '../components/LandingPic.vue';

export default {
  name: 'MainPage',
  components: {
    Landing,
    SocialMedia,
    CodingSkills,
    CodingTools,
    WorkExperience,
    Education,
    Projects,
    GitHubStats,
    ContactMe,
    Footer,
    AboutMe,
    ProfilePic,
    LandingPic,
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
.section {
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
</style>
