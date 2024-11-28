<template>
  <v-container fluid class="text-center my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Education</span>
    </h2>
    <v-row justify="center">
      <v-col cols="12" md="10">
        <v-card
            v-for="(education, index) in educations"
            :key="index"
            class="education-card my-5"
            outlined
        >
          <v-row class="align-center">
            <v-col cols="2" class="text-center">
              <v-icon :size="40" :style="{ color: education.iconColor }">
                {{ education.icon }}
              </v-icon>
            </v-col>
            <v-col cols="8">
              <div class="d-flex align-center">
                <h3 class="education-major ml-2">
                  {{ education.major }}
                </h3>
              </div>
              <span>
                <v-chip
                    small
                    color="blue lighten-4"
                    text-color="blue darken-2"
                >
                  {{ education.type }}
                </v-chip>
                <v-chip
                    small
                    class="ml-2"
                    color="green lighten-4"
                    text-color="green darken-2"
                >
                  {{ education.degreeType }}
                </v-chip>
              </span>
              <span class="education-school">
                {{ education.school }}
              </span>
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
            <v-col cols="2" class="text-right">
              <div class="education-date">
                {{ education.date }}
              </div>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Education',
  data() {
    return {
      educations: [
        {
          degreeType: 'Bachelor of Science',
          major: 'Computer Science',
          school: 'University at Buffalo, State University of New York',
          location: 'Buffalo, New York',
          date: 'Jan 2022 - Present',
          description: 'Description',
          icon: 'mdi-school',
          iconColor: 'purple',
          type: 'Undergraduate',
        },
        {
          degreeType: 'Bachelor of Business Administration',
          major:
              'Management Information Systems and Supply Chain Management',
          school: 'University at Buffalo, State University of New York',
          location: 'Buffalo, New York',
          date: 'Jan 2022 - Present',
          description: 'Description',
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
  width: 600px;
  height: 200px;
  margin-left: -75px;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 12px;
  transition: transform 0.3s, background-color 0.3s;
}

.education-card:hover {
  transform: scale(1.02);
  background-color: #f9f9f9;
}

.education-major {
  font-weight: 500;
  font-size: 16px;
  margin-bottom: 8px;
}

.education-school {
  display: block;
  font-size: 12px;
  color: #757575;
  margin-top: 4px;
}

.education-location,
.education-date {
  font-size: 12px;
  color: #757575;
}

.education-description {
  font-size: 16px;
  color: #424242;
  margin-top: 8px;
}

.v-icon {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
