<template>
  <v-card flat class="landing-container">
    <h1 class="name">// Alex Feng //</h1>
    <h2 class="headline">{{ displayedText }}</h2>
    <div class="social-media-container">
      <SocialMedia />
    </div>
  </v-card>
</template>

<script>
import SocialMedia from '../components/SocialMedia.vue';

export default {
  name: 'Landing',
  components: {
    SocialMedia,
  },
  data() {
    return {
      texts: ['Software Engineer', 'Research Assistant', 'Teaching Assistant', 'Web Developer', 'Procurement Director'],
      displayedText: '',
      textIndex: 0,
      charIndex: 0,
      isDeleting: false,
      typingSpeed: 120,
      pauseDuration: 500,
    };
  },
  mounted() {
    this.typeWriter();
  },
  methods: {
    typeWriter() {
      const currentText = this.texts[this.textIndex];
      if (this.isDeleting) {
        this.displayedText = currentText.substring(0, this.charIndex--);
      } else {
        this.displayedText = currentText.substring(0, this.charIndex++);
      }

      if (!this.isDeleting && this.charIndex === currentText.length) {
        this.isDeleting = true;
        setTimeout(this.typeWriter, this.pauseDuration);
        return;
      } else if (this.isDeleting && this.charIndex === 0) {
        this.isDeleting = false;
        this.textIndex = (this.textIndex + 1) % this.texts.length;
      }

      setTimeout(this.typeWriter, this.isDeleting ? this.typingSpeed / 2 : this.typingSpeed);
    },
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Saira:wght@400;700&display=swap');

.landing-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  font-family: 'Saira', sans-serif;
  text-align: center;
}

.name {
  font-size: 6.5rem;
  font-weight: 500;
  margin: 0;
  color: #000;
}

.headline {
  font-size: 2rem;
  font-weight: 400;
  margin: 0.5rem 0;
  color: #000;
  min-height: 2.5em;
}

.social-media-container {
  margin-top: 1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0.5rem;
  border: 1px solid #000;
  border-radius: 8px;
  width: fit-content;
}
</style>
