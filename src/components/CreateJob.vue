<template>
  <div class="create-job border col-12">
    <form @submit.prevent="createJob()">
      <div class="form-group">
        <label for="jobTitle">Job Title</label>
        <input type="text" name="jobTitle" id="" class="form-control" placeholder="enter job title..." aria-describedby="helpId"
          v-model="newJob.jobTitle" required>
      </div>
      <div class="form-group">
        <label for="company">Employer</label>
        <input type="text" name="company" id="" class="form-control" placeholder="enter company..."
          aria-describedby="helpId" v-model="newJob.company" required>
      </div>
      <div class="form-group">
        <label for="hours">Hours</label>
        <input type="number" name="hours" id="" class="form-control" placeholder="enter expected hours..."
          aria-describedby="helpId" v-model="newJob.hours" required>
      </div>
      <div class="form-group">
        <label for="rate">Hourly Rate</label>
        <input type="number" name="rate" id="" class="form-control" placeholder="enter wage..."
          aria-describedby="helpId" v-model="newJob.rate" required>
      </div>
      <button type="submit" class="btn btn-success"> Add Job</button>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'create-job',
    data() {
      return {
        newJob: {}
      }
    },
    methods: {
      createJob() {
        this.$store.dispatch('createJob', this.newJob)
        this.newJob = {}
      }
    }
  }
</script>

<style>
  .create-job {
    outline: 1px solid black;
  }
</style>