<script>
export default {
  data() {
    return {};
  },

  props: {
    project: Object,
  },
};
</script>

<template>
  <div class="col">
    <div class="card h-100">
      <div class="card-body">
        <h3>{{ project.title }}</h3>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
