<template>
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Education</span>
    </h2>
    <v-row>
      <v-col cols="12" md="10">
        <v-card
            v-for="(education, index) in educations"
            :key="index"
            class="education-card my-10"
        >
          <div class="education-header"></div>
          <v-row class="align-start">
            <v-col cols="2" class="text-left logo-col">
              <v-img :src="education.image" max-width="120" class="education-logo"></v-img>
            </v-col>
            <v-col cols="10" class="text-left">
              <div class="education-school-name">{{ education.school }}</div>
              <div class="education-major-title">{{ education.major }}</div>
              <div class="education-date">{{ education.date }}</div>
              <div class="education-location d-flex align-center mt-2">
                <v-icon color="grey darken-1" size="20" class="mr-1">mdi-map-marker</v-icon>
                {{ education.location }}
              </div>
              <div class="education-description mt-3">
                {{ education.description }}
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import NorthCampus from "@/assets/buffalo.png";

export default {
  name: 'Education',
  data() {
    return {
      educations: [
        {
          degreeType: 'Bachelor of Science',
          major: 'BS - Computer Science',
          school: 'University at Buffalo, State University of New York',
          location: 'Buffalo, New York',
          date: 'Jan 2022 - Present',
          description: 'Relevant Courses:',
          image: NorthCampus,
          icon: 'mdi-school',
          iconColor: 'purple',
          type: 'Undergraduate',
        },
        {
          degreeType: 'Bachelor of Business Administration',
          major:
              'BBA - Management Information Systems and Supply Chain Management',
          school: 'University at Buffalo, State University of New York',
          location: 'Buffalo, New York',
          date: 'Jan 2022 - Present',
          description: 'Relevant Courses:',
          image: NorthCampus,
          icon: 'mdi-school',
          iconColor: 'green',
          type: 'Undergraduate',
        },
      ],
    };
  },
};
</script>

<style scoped>
.education-card {
  position: relative;
  padding: 120px 0 40px;
  background-color: #fff;
  border-bottom: 1px solid #e0e0e0;
  box-shadow: none;
  border-radius: 0;
  text-align: left;
}

.education-header {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 120px;
  background: url('../assets/campus.png') center center/cover no-repeat;
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
}

.logo-col {
  position: relative;
  z-index: 1;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  margin-top: -60px;
  margin-left: 5px;
}

.education-logo {
  border-radius: 50%;
  border: 1px solid #fff;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
}

.education-school-name {
  font-size: 28px;
  font-weight: 700;
  margin-bottom: 12px;
  word-wrap: break-word;
}

.education-major-title {
  font-size: 20px;
  font-weight: 500;
  margin-bottom: 12px;
  word-wrap: break-word;
}

.education-date,
.education-location {
  font-size: 16px;
  color: #757575;
}

.education-description {
  font-size: 16px;
  color: #424242;
  margin-top: 16px;
  word-wrap: break-word;
}

.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
