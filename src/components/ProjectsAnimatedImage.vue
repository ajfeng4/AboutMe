<template>
  <v-container class="text-center my-10">
    <img
        :src="giphyUrl"
        alt="Projects Animated illustration"
        class="animated-image"
    />
  </v-container>
</template>

<script>
export default {
  name: "ProjectsAnimatedImage",
  props: {
    giphyUrl: {
      type: String,
      default: "https://media.giphy.com/media/RjZM6XvmRBZ30xbcWy/giphy.gif",
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
