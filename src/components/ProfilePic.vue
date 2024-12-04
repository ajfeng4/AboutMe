<template>
  <v-container class="text-center my-10">
    <img
        :src="profilePicUrl"
        alt="Profile Picture"
        class="profile-pic"
    />
  </v-container>
</template>

<script>
import profilePic from '@/assets/davis.png';

export default {
  name: "ProfilePic",
  data() {
    return {
      profilePicUrl: profilePic,
    };
  },
};
</script>

<style scoped>
.profile-pic {
  max-width: 100%;
  height: auto;
  border-radius: 16px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
