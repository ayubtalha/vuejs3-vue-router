<template>
  <h1>jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <!-- PARAMS FOR SENDING ID TO ROUTE -->
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2>
        {{ job.title }}
      </h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          title: "Web",
          id: 1,
          details: "Software",
        },
        {
          title: "Developer",
          id: 2,
          details: "Software",
        },
        {
          title: "Software Developer",
          id: 3,
          details: "Software",
        },
      ],
    };
  },
};
</script>

<style>
.job h2 {
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h2:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
