<template>
  <div class="job border col-3">
    <h5>{{jobData.jobTitle}}</h5>
    <h5>{{jobData.company}}</h5>
    <p>{{jobData.hours}}</p>
    <p>${{jobData.rate}}</p>
    <button class="btn btn-danger mb-1" @click="deleteJob()">Delete</button>
  </div>
</template>

<script>
  export default {
    name: 'job',
    props: ["jobData"],
    data() {
      return {
      }
    },
    methods: {
      deleteJob() {
        this.$store.dispatch("deleteJob", this.jobData._id)
      }
    }
  }
</script>

<style>
  .job {
    outline: 1px solid black;
  }
</style>