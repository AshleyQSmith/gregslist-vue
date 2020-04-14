<template>
  <div class="home container-fluid">
    <!-- cars -->
    <div class="row">
      <Cars></Cars>
    </div>
    <!-- houses -->
    <div class="row">
      <Houses></Houses>
    </div>
        <!-- jerbs -->
    <div class="row">
      <Jobs></Jobs>
    </div>

  </div>
</template>

<script>
  import Cars from '../components/Cars.vue'
  import Houses from '../components/Houses.vue'
  import Jobs from '../components/Jobs.vue'
  export default {
    name: 'Home',
    components: { Cars, Houses, Jobs }
  }
</script>