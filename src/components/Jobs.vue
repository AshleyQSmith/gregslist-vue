<template>
  <div class="jobs col-12">
    <!-- i will build a bunch of job components for each-->
    <div class="row">
      <create-job></create-job>
      <job v-for="job in jobs" :jobData="job"></job>
      <!-- job deetz go here -->
    </div>
  </div>
</template>

<script>
  import Job from './Job.vue'
  import CreateJob from './CreateJob.vue'
  export default {
    name: 'jobs',
    data() {
      return {
      }
    },
    computed: {
      jobs() {
        return this.$store.state.jobs
      }
    },
    created() {
      this.$store.dispatch("getJobs")
    },
    methods: {},
    components: {
      Job,
      CreateJob
    }
  }
</script>

<style>
  .jobs {
    outline: 1px solid black;
  }
</style>