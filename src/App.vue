<script>
import ProjectList from "./components/projects/ProjectList.vue";
import axios from "axios";

export default {
  data() {
    return {
      projects: [],

      api: {
        baseUrl: "http://127.0.0.1:8000/api/",
      },
    };
  },

  components: { ProjectList },

  methods: {
    fetchProjects(uri = this.api.baseUrl + "projects") {
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
  <h1>HELLO</h1>
  <hr />
  <ProjectList></ProjectList>
</template>
<style lang="scss"></style>
