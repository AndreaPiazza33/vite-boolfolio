<script>
import ProjectList from "./components/projects/ProjectList.vue";
import axios from "axios";
import { store } from "./data/store";

export default {
  data() {
    return {
      projects: [],
    };
  },

  components: { ProjectList },

  methods: {
    fetchProjects(uri = store.api.baseUrl + "projects") {
      axios.get(uri).then((response) => {
        this.projects = response.data.data;
      });
    },
  },
  created() {
    this.fetchProjects();
  },
};
</script>
<template>
  <h1 class="mx-3 my-3 text-info">BOOLFOLIO</h1>
  <hr />
  <ProjectList :projects="projects"></ProjectList>
</template>
<style lang="scss"></style>
