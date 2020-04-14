<template>
  <div class="car border col-3">
    <img class="img-fluid" :src="carData.imgUrl" alt="" srcset="">
    <h5>{{carData.make}}</h5>
    <h5>{{carData.model}}</h5>
    <p>{{carData.price}}</p>
    <p>{{carData.year}}</p>
    <button class="btn btn-danger mb-1" @click="deleteCar()">Delete</button>
  </div>
</template>

<script>
  export default {
    name: 'car',
    props: ["carData"],
    data() {
      return {
      }
    },
    methods: {
      deleteCar() {
        this.$store.dispatch("deleteCar", this.carData._id)
      }
    }
  }
</script>

<style>
  .cars {
    outline: 1px solid black;
  }
</style>