<template>
  <v-container>
    <div id="about">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="6">
          <Landing />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <ProfilePic />
        </v-col>
      </v-row>
    </div>

    <v-row class="my-10">
      <v-col cols="12" md="6">
        <AboutMe />
      </v-col>
      <v-col cols="12" md="6" class="text-center">
        <LandingPic />
      </v-col>
    </v-row>

    <v-row class="my-10">
      <v-col cols="12" md="6" class="text-center">
        <AnimatedImage />
      </v-col>
      <v-col cols="12" md="6">
        <CodingSkills />
      </v-col>
    </v-row>

    <v-row>
      <v-col cols="12">
        <v-spacer class="custom-spacer"></v-spacer>
      </v-col>
    </v-row>

    <div id="tools">
      <CodingTools />
    </div>

    <div id="education">
      <v-row class="my-12">
        <v-col cols="12" md="6">
          <Education />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <EducationAnimatedImage />
        </v-col>
      </v-row>
    </div>

    <div id="experience">
      <v-row class="my-12">
        <v-col cols="12" md="6" class="text-center">
          <ExperienceAnimatedImage />
        </v-col>
        <v-col cols="12" md="6">
          <WorkExperience />
        </v-col>
      </v-row>
    </div>

    <div id="projects">
      <v-row class="my-12">
        <v-col cols="12" md="6">
          <Projects />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <ProjectsAnimatedImage />
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

    <Footer />
  </v-container>
</template>

<script>
import Landing from '../components/Landing.vue';
import SocialMedia from '../components/SocialMedia.vue';
import CodingSkills from '../components/CodingSkills.vue';
import AnimatedImage from '../components/AnimatedImage.vue';
import EducationAnimatedImage from '../components/EducationAnimatedImage.vue';
import ExperienceAnimatedImage from '../components/ExperienceAnimatedImage.vue';
import ProjectsAnimatedImage from '../components/ProjectsAnimatedImage.vue';
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
    AnimatedImage,
    EducationAnimatedImage,
    ExperienceAnimatedImage,
    ProjectsAnimatedImage,
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
</style>