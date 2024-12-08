<template>
  <div style="width:100%;margin:0;padding:0;">
    <div id="about" class="section-gradient">
      <v-row align="center" justify="center" class="my-10">
        <v-col cols="12" md="6">
          <Landing />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <ProfilePic />
        </v-col>
      </v-row>
    </div>

    <div id="landing-section" class="section-gradient">
      <v-row class="my-10">
        <v-col cols="12" md="6">
          <AboutMe />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <LandingPic />
        </v-col>
      </v-row>
    </div>

    <div id="skills-section" class="section-gradient">
      <v-row class="my-10">
        <v-col cols="12" md="6" class="text-center">
          <AnimatedImage />
        </v-col>
        <v-col cols="12" md="6">
          <CodingSkills />
        </v-col>
      </v-row>
    </div>

    <div id="spacer-section" class="section-gradient">
      <v-row>
        <v-col cols="12">
          <v-spacer class="custom-spacer"></v-spacer>
        </v-col>
      </v-row>
    </div>

    <div id="tools" class="section-gradient">
      <CodingTools />
    </div>

    <div id="education" class="section-gradient">
      <v-row class="my-12">
        <v-col cols="12" md="6">
          <Education />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <EducationAnimatedImage />
        </v-col>
      </v-row>
    </div>

    <div id="experience" class="section-gradient">
      <v-row class="my-12">
        <v-col cols="12" md="6" class="text-center">
          <ExperienceAnimatedImage />
        </v-col>
        <v-col cols="12" md="6">
          <WorkExperience />
        </v-col>
      </v-row>
    </div>

    <div id="projects" class="section-gradient">
      <v-row class="my-12">
        <v-col cols="12" md="6">
          <Projects />
        </v-col>
        <v-col cols="12" md="6" class="text-center">
          <ProjectsAnimatedImage />
        </v-col>
      </v-row>
    </div>

    <div id="github-stats" class="section-gradient">
      <v-row class="my-12">
        <v-col cols="12">
          <GitHubStats />
        </v-col>
      </v-row>
    </div>

    <div id="contact" class="section-gradient">
      <ContactMe />
    </div>

    <Footer />
  </div>
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
#about {
  background: linear-gradient(to right, #e0f7fa, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#landing-section {
  background: linear-gradient(to right, #fff9c4, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#skills-section {
  background: linear-gradient(to right, #fce4ec, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#spacer-section {
  background: linear-gradient(to right, #c8e6c9, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#tools {
  background: linear-gradient(to right, #ffe0b2, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#education {
  background: linear-gradient(to right, #d1c4e9, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#experience {
  background: linear-gradient(to right, #bbdefb, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#projects {
  background: linear-gradient(to right, #ffccbc, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#github-stats {
  background: linear-gradient(to right, #d7ccc8, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
#contact {
  background: linear-gradient(to right, #b2ebf2, #ffffff);
  padding: 20px;
  margin: 0;
  width: 100%;
  box-sizing: border-box;
}
</style>