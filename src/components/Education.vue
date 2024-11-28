<template>
  <v-container class="text-center my-10">
    <h2 class="display-2 font-weight-bold">
      My <span style="font-weight: 900;">Education</span>
    </h2>
    <v-row justify="center" align="center">
      <v-col
          v-for="(education, index) in educations"
          :key="index"
          cols="12"
          sm="6"
          md="4"
          class="d-flex justify-center align-center"
      >
        <div
            class="education-card"
            @mouseover="hoverEducation = index"
            @mouseleave="hoverEducation = null"
        >
          <v-icon
              :size="60"
              class="mb-2"
              :style="{ color: hoverEducation === index ? education.iconColor : '#b0b0b0' }"
          >
            {{ education.icon }}
          </v-icon>
          <h3
              class="education-degree"
              :style="{ color: hoverEducation === index ? '#000' : '#b0b0b0' }"
          >
            {{ education.degree }}
          </h3>
          <span
              class="education-school"
              :style="{ color: hoverEducation === index ? '#000' : '#b0b0b0' }"
          >
            {{ education.school }}
          </span>
          <span
              class="education-location"
              :style="{ color: hoverEducation === index ? '#000' : '#b0b0b0' }"
          >
            {{ education.location }}
          </span>
          <span
              class="education-date"
              :style="{ color: hoverEducation === index ? '#000' : '#b0b0b0' }"
          >
            {{ education.date }}
          </span>
          <p
              class="education-description"
              :style="{ color: hoverEducation === index ? '#000' : '#b0b0b0' }"
          >
            {{ education.description }}
          </p>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Education',
  data() {
    return {
      hoverEducation: null,
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
.education-card {
  text-align: center;
  padding: 16px;
  transition: transform 0.3s;
}

.education-card:hover {
  transform: scale(1.05);
}

.education-degree {
  display: block;
  margin-top: 8px;
  font-weight: 600;
  font-size: 16px;
}

.education-school,
.education-location,
.education-date,
.education-description {
  display: block;
  margin-top: 4px;
  font-size: 14px;
}
</style>
