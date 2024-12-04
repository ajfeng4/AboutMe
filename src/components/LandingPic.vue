<template>
  <v-container class="text-center my-10">
    <img
        :src="landingPicUrl"
        alt="Landing Picture"
        class="landing-pic"
    />
  </v-container>
</template>

<script>
import landingPic from '@/assets/Me.png';

export default {
  name: "LandingPic",
  data() {
    return {
      landingPicUrl: landingPic,
    };
  },
};
</script>

<style scoped>
.landing-pic {
  max-width: 100%;
  height: auto;
  border-radius: 16px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>