<template>
  <v-container fluid class="text-left my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Education</span>
    </h2>
    <div class="scrollable-education">
      <v-row justify="center">
        <v-col cols="12" md="10">
          <v-card
              v-for="(education, index) in educations"
              :key="index"
              class="education-card my-5"
              outlined
          >
            <v-row class="align-start">
              <v-col cols="2" class="text-left">
                <v-img :src="education.image" max-width="200"></v-img>
              </v-col>
              <v-col cols="10" class="text-left">
                <div class="d-flex justify-space-between align-start">
                  <div class="education-details">
                    <h3 class="education-major ml-2">
                      {{ education.major }}
                    </h3>
                    <span class="education-school">
                      {{ education.school }}
                    </span>
                  </div>
                  <div class="education-date">
                    {{ education.date }}
                  </div>
                </div>
                <div class="d-flex align-center mt-2">
                  <v-icon
                      color="grey darken-1"
                      size="20"
                      class="mr-1"
                  >mdi-map-marker</v-icon>
                  <span class="education-location">
                    {{ education.location }}
                  </span>
                </div>
                <p class="education-description mt-3">
                  {{ education.description }}
                </p>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
import NorthCampus from "@/assets/northcampus.png";

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
  padding: 24px;
  background-color: #fff;
  width: 120%;
  height: 150px;
  margin-left: -50px;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 12px;
  text-align: left;
}

.education-major {
  font-weight: 500;
  font-size: 12px;
  margin-bottom: 8px;
  word-wrap: break-word;
}

.education-school {
  display: block;
  font-size: 12px;
  color: #757575;
  margin-top: 4px;
  word-wrap: break-word;
}

.education-location,
.education-date {
  font-size: 12px;
  color: #757575;
  white-space: nowrap;
}

.education-date {
  flex-shrink: 0;
  margin-left: 8px;
}

.education-description {
  font-size: 12px;
  color: #424242;
  margin-top: 8px;
  word-wrap: break-word;
}

.education-details {
  flex: 1;
  min-width: 0;
  text-align: left;
}

.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}

.v-img {
  margin-right: auto;
}

.scrollable-education {
  max-height: 420px;
  overflow-y: auto;
  overflow-x: hidden;
}

/* Scrollbar Styles */
.scrollable-education::-webkit-scrollbar {
  width: 8px;
}

.scrollable-education::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 4px;
}

.scrollable-education::-webkit-scrollbar-thumb {
  background: #c1c1c1;
  border-radius: 4px;
}

.scrollable-education::-webkit-scrollbar-thumb:hover {
  background: #a8a8a8;
}

.scrollable-education {
  scrollbar-width: thin;
  scrollbar-color: #c1c1c1 #f1f1f1;
}
</style>
