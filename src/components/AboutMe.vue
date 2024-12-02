<template>
  <div class="aboutme-container">
    <div class="aboutme-content">
      <h1 class="aboutme-title">About Me</h1>
      <h2 class="aboutme-heading">I'm Alex</h2>
      <p class="aboutme-subheading">Full Stack Developer</p>
      <p class="aboutme-body">
        A full-time student taking a full course load and working 40 hours a week. Passionate about front-end and mobile development,
        with experience in technical and non-technical environments. An experienced team player and seasoned leader.
      </p>
      <p class="aboutme-details">
        <span>Email:</span> ajfengcs@gmail.com <br />
        <span>Place:</span> Brooklyn, NY
      </p>
      <button class="resume-button">Resume ›</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMe',
};
</script>

<style scoped>
.aboutme-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: 100%;
  text-align: center;
}

.aboutme-content {
  max-width: 600px;
  padding: 20px;
  border-radius: 8px;
}

.aboutme-title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.aboutme-heading {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.aboutme-subheading {
  font-size: 1.2rem;
  font-weight: 600;
  color: #555;
  margin-bottom: 1rem;
}

.aboutme-body {
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  color: #333;
}

.aboutme-details span {
  font-weight: bold;
  color: #444;
}

.resume-button {
  background-color: #007bff;
  color: white;
  padding: 0.75rem 1.5rem;
  font-size: 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

.resume-button:hover {
  background-color: #0056b3;
}
</style>
