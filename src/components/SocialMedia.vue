<template>
  <v-row class="mb-4" align="center" justify="center" style="flex-wrap: nowrap;">
    <v-btn
        v-for="(media, index) in socialMedia"
        :key="index"
        class="social-btn"
        :style="{ backgroundColor: media.color, width: 'auto' }"
        :href="media.link"
        :target="media.isEmail ? '_self' : '_blank'"
        text
    >
      <v-icon class="mr-2" size="18">{{ media.icon }}</v-icon>
      <span class="social-text">{{ media.name }}</span>
    </v-btn>
  </v-row>
</template>

<script>
export default {
  name: 'SocialMedia',
  data() {
    return {
      socialMedia: [
        { icon: 'mdi-github', name: 'GitHub', color: '#333', link: 'https://github.com/ajfeng4' },
        { icon: 'mdi-linkedin', name: 'LinkedIn', color: '#0077b5', link: 'https://www.linkedin.com/in/ajfeng/' },
        { icon: 'mdi-medium', name: 'Medium', color: '#000000', link: 'https://medium.com/' },
        { icon: 'mdi-gmail', name: 'Gmail', color: '#D14836', link: 'mailto:ajfengcs@gmail.com', isEmail: true },
        { icon: 'mdi-outlook', name: 'Outlook', color: '#0072C6', link: 'mailto:ajfeng@buffalo.edu', isEmail: true },
      ],
    };
  },
};
</script>

<style scoped>
.social-btn {
  display: inline-flex;
  align-items: center;
  margin: 4px;
  color: white;
  border-radius: 20px;
  padding: 6px 12px;
  text-decoration: none;
  white-space: nowrap;
}

.social-btn:hover {
  opacity: 0.9;
}

.social-text {
  font-size: 12px;
  font-weight: 500;
}
</style>
