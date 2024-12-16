<template>
  <div style="width:100%;margin:0;padding:0;">
    <div id="about" class="section" v-show-on-scroll>
      <v-row class="my-10">
        <v-col cols="12">
          <Landing />
        </v-col>
        <v-col cols="12">
          <ProfilePic />
        </v-col>
      </v-row>
    </div>

    <div id="landing-section" class="section" v-show-on-scroll>
      <v-row class="my-10">
        <v-col cols="12">
          <AboutMe />
        </v-col>
        <v-col cols="12">
          <LandingPic />
        </v-col>
      </v-row>
    </div>

    <div id="skills-section" class="section" v-show-on-scroll>
      <v-row class="my-10">
        <v-col cols="12">
          <CodingSkills />
        </v-col>
      </v-row>
    </div>

    <div id="spacer-section" class="section" v-show-on-scroll>
      <v-row>
        <v-col cols="12">
          <v-spacer class="custom-spacer"></v-spacer>
        </v-col>
      </v-row>
    </div>

    <div id="tools" class="section" v-show-on-scroll>
      <v-row class="my-10">
        <v-col cols="12">
          <CodingTools />
        </v-col>
      </v-row>
    </div>

    <div id="education" class="section" v-show-on-scroll>
      <v-row class="my-12">
        <v-col cols="12">
          <Education />
        </v-col>
      </v-row>
    </div>

    <div id="experience" class="section" v-show-on-scroll>
      <v-row class="my-12">
        <v-col cols="12">
          <WorkExperience />
        </v-col>
      </v-row>
    </div>

    <div id="projects" class="section" v-show-on-scroll>
      <v-row class="my-12">
        <v-col cols="12">
          <Projects />
        </v-col>
      </v-row>
    </div>

    <div id="github-stats" class="section" v-show-on-scroll>
      <v-row class="my-12">
        <v-col cols="12">
          <GitHubStats />
        </v-col>
      </v-row>
    </div>

    <div id="contact" class="section" v-show-on-scroll>
      <v-row class="my-10">
        <v-col cols="12">
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
  directives: {
    showOnScroll: {
      mounted(el) {
        el.style.opacity = '0';
        const observer = new IntersectionObserver((entries) => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              el.style.transition = 'opacity 1s ease-in-out';
              el.style.opacity = '1';
              observer.unobserve(el);
            }
          });
        });
        observer.observe(el);
      }
    }
  }
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
  margin: 0;
  width: 100%;
  box-sizing: border-box;
  padding:0;
}
</style>