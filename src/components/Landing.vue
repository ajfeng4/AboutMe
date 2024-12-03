<template>
  <v-card flat>
    <h1 class="display-2 font-weight-bold mb-3">Hello, I'm Alex Feng</h1>
    <h2 class="headline font-weight-bold">{{ displayedText }}</h2>
    <SocialMedia />
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
      texts: ['Computer Science Student', 'Software Engineer', 'Diretor of Procurement', 'Web Developer Assistant','Teaching Assistant','Research Assistant'],
      displayedText: '',
      textIndex: 0,
      charIndex: 0,
      isDeleting: false,
      typingSpeed: 100,
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

      if (!this.isDeleting && this.charIndex > currentText.length) {
        this.isDeleting = true;
        this.typingSpeed = 100;
      } else if (this.isDeleting && this.charIndex < 0) {
        this.isDeleting = false;
        this.textIndex = (this.textIndex + 1) % this.texts.length;
        this.charIndex = 0;
        this.typingSpeed = 100;
      }

      setTimeout(this.typeWriter, this.typingSpeed);
    },
  },
};
</script>

<style scoped>
.headline {
  min-height: 2.5em;
}
</style>