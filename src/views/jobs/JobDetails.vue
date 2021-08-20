<template>
  <div v-if="job">
    <h1>JobDetails Page</h1>
    <p>The Job Title is {{ job.title }}</p>
    <p>The Job ID is {{ job.id }}</p>
    <p>The Job Details is {{ job.details }}</p>
  </div>
  <div v-else>
    <h1>JobDetails Page</h1>
    <p>Loading Job Details</p>
  </div>
</template>

<script>
export default {
  props: ["id"],
  data() {
    return { job: null };
  },
  mounted() {
    fetch("http://localhost:3000/jobs/" + this.id)
      .then((res) => res.json())
      .then((data) => (this.job = data))
      .catch((err) => console.log(err.message));
  },
};
</script>

<style></style>
