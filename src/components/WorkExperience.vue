<template>
  <v-container>
    <v-row align="center" justify="center" class="my-10">
      <v-col cols="12" md="10">
        <v-card flat>
          <h1 class="display-2 font-weight-bold mb-5">My Experience</h1>

          <v-card
              v-for="(experience, index) in experiences"
              :key="index"
              outlined
              elevation="2"
              class="experience-card mb-5 py-4 px-6"
          >
            <v-row>
              <v-col cols="1" class="d-flex align-center justify-center">
                <v-icon :color="experience.iconColor" size="40">{{ experience.icon }}</v-icon>
              </v-col>
              <v-col cols="11">
                <v-row>
                  <v-col cols="8" class="d-flex align-center">
                    <h3 class="font-weight-bold">
                      {{ experience.title }}
                    </h3>
                    <v-chip
                        v-if="experience.type"
                        class="ml-3"
                        color="blue lighten-4"
                        text-color="blue darken-2"
                        small
                    >
                      {{ experience.type }}
                    </v-chip>
                  </v-col>
                </v-row>

                <v-row align="center" class="mt-2">
                  <v-col cols="4" class="d-flex align-center">
                    <v-icon color="grey darken-1" size="20" class="mr-2">mdi-office-building</v-icon>
                    <span>{{ experience.company }}</span>
                  </v-col>
                  <v-col cols="4" class="d-flex align-center">
                    <v-icon color="grey darken-1" size="20" class="mr-2">mdi-map-marker</v-icon>
                    <span>{{ experience.location }}</span>
                  </v-col>
                  <v-col cols="4" class="d-flex align-center justify-end">
                    <v-icon color="grey darken-1" size="20" class="mr-2">mdi-calendar</v-icon>
                    <span>{{ experience.date }}</span>
                  </v-col>
                </v-row>

                <p class="text--secondary mt-3">{{ experience.description }}</p>
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
  name: 'WorkExperience',
  data() {
    return {
      experiences: [
        {
          title: 'Position Title',
          company: 'Company Name',
          location: 'City, State',
          date: 'Start Date - End Date',
          description: 'Brief description of the role and responsibilities, highlighting key achievements and contributions...',
          icon: 'mdi-briefcase',
          iconColor: 'blue',
          type: 'Full-Time',
        },
        {
          title: 'Position Title',
          company: 'Company Name',
          location: 'City, State',
          date: 'Start Date - End Date',
          description: 'Brief description of the role and responsibilities, highlighting key achievements and contributions...',
          icon: 'mdi-briefcase',
          iconColor: 'green',
          type: 'Part-Time',
        },
        {
          title: 'Position Title',
          company: 'Company Name',
          location: 'City, State',
          date: 'Start Date - End Date',
          description: 'Brief description of the role and responsibilities, highlighting key achievements and contributions...',
          icon: 'mdi-briefcase',
          iconColor: 'orange',
          type: 'Internship',
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
.experience-card {
  transition: transform 0.3s, background-color 0.3s;
  background-color: #f9f9f9;
}

.experience-card:hover {
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
