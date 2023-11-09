<script>
import ProjectCard from "./ProjectCard.vue";

export default {
  data() {
    return {};
  },

  components: { ProjectCard },

  props: {
    projects: Array,
  },
};
</script>

<template>
  <div class="container">
    <h2 class="my-3">PostList:</h2>
    <div class="row row-cols-2 g-3">
      <ProjectCard v-for="project in projects" :project="project"></ProjectCard>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
