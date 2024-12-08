<template>
  <v-container class="text-center my-10">
    <img
        :src="giphyUrl"
        alt="Education illustration"
        class="animated-image"
    />
  </v-container>
</template>

<script>
export default {
  name: "EducationAnimatedImage",
  props: {
    giphyUrl: {
      type: String,
      default: "https://media.giphy.com/media/PyNo0O6NqwMTTeZjd3/giphy.gif",
    },
  },
};
</script>

<style scoped>
.animated-image {
  max-width: 100%;
  height: auto;
  border-radius: 16px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
