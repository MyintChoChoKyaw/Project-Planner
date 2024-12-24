<template>
  <div class="home">
    <h1>Projects</h1>
    <div v-for="project in projects" :key="project.id">
      <SingleProjectVue :project="project"></SingleProjectVue>
    </div>
  </div>
</template>

<script>
import SingleProjectVue from '../components/SingleProject.vue';

export default {
  name: "HomeView",
  components: {
    SingleProjectVue
  },
  data() {
    return {
      projects: [],
    };
  },
  mounted() {
    fetch("http://localhost:3000/projects")
      .then((resolve) => {
        return resolve.json();
      })
      .then((data) => {
        this.projects = data;
      });
  },
};
</script>
