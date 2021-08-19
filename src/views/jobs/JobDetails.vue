<template>
  <h1>JobDetails Page</h1>
  <!-- ROUTE OBJECT -->
  <p>The Job ID is {{ id }}</p>
  <!-- ROUTE PARAMS AS PROPS -->
  <p>The Job ID via PROPS is {{ id }}</p>
</template>

<script>
export default {
  // ROUTE PARAMS AS PROPS
  props: ["id"],
  // ROUTE OBJECT
  //   data() {
  //     return {
  //       id: this.$route.params.id,
  //     };
  //   },
};
</script>

<style></style>
