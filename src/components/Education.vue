<template>
  <v-container>
    <v-row align="center" justify="center" class="my-10">
      <v-col cols="12" md="10">
        <v-card flat>
          <h1 class="display-2 font-weight-bold mb-5">My Education</h1>

          <v-card
              v-for="(education, index) in educations"
              :key="index"
              outlined
              elevation="2"
              class="education-card mb-5 py-4 px-6"
          >
            <v-row>
              <v-col cols="1" class="d-flex align-center justify-center">
                <v-icon :color="education.iconColor" size="40">{{ education.icon }}</v-icon>
              </v-col>
              <v-col cols="11">
                <v-row>
                  <v-col cols="8" class="d-flex align-center">
                    <h3 class="font-weight-bold">
                      {{ education.degree }}
                    </h3>
                    <v-chip
                        v-if="education.type"
                        class="ml-3"
                        color="blue lighten-4"
                        text-color="blue darken-2"
                        small
                    >
                      {{ education.type }}
                    </v-chip>
                  </v-col>
                </v-row>

                <v-row align="center" class="mt-2">
                  <v-col cols="4" class="d-flex align-center">
                    <v-icon color="grey darken-1" size="20" class="mr-2">mdi-school</v-icon>
                    <span>{{ education.school }}</span>
                  </v-col>
                  <v-col cols="4" class="d-flex align-center">
                    <v-icon color="grey darken-1" size="20" class="mr-2">mdi-map-marker</v-icon>
                    <span>{{ education.location }}</span>
                  </v-col>
                  <v-col cols="4" class="d-flex align-center justify-end">
                    <v-icon color="grey darken-1" size="20" class="mr-2">mdi-calendar</v-icon>
                    <span>{{ education.date }}</span>
                  </v-col>
                </v-row>

                <p class="text--secondary mt-3">{{ education.description }}</p>
              </v-col>
            </v-row>
          </v-card>
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
          degree: 'Bachelor of Science in Computer Science',
          school: 'University at Buffalo, State University of New York',
          location: 'Buffalo, New York',
          date: 'Jan 2022 - Present',
          description: 'Description',
          icon: 'mdi-school',
          iconColor: 'purple',
          type: 'Undergraduate',
        },
        {
          degree: 'Bachelor of Business Administration in Management Information Systems and Supply Chain Management',
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
.display-2 {
  color: #333;
}
.font-weight-bold {
  font-weight: 700;
}
.education-card {
  transition: transform 0.3s, background-color 0.3s;
  background-color: #f9f9f9;
}

.education-card:hover {
  transform: scale(1.05);
  background-color: #333;
  color: #fff;
}

.v-icon,
.font-weight-medium,
.text--secondary {
  color: inherit;
}
</style>