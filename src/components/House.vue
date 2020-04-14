<template>
  <div class="house border col-3">
    <img class="img-fluid" :src="houseData.imgUrl" alt="" srcset="">
    <h5>{{houseData.bedrooms}} Beds</h5>
    <h5>{{houseData.bathrooms}} Baths</h5>
    <p>${{houseData.price}}</p>
    <p>{{houseData.year}}</p>
    <button class="btn btn-danger mb-1" @click="deleteHouse()">Delete</button>
  </div>
</template>

<script>
  export default {
    name: 'house',
    props: ["houseData"],
    data() {
      return {
      }
    },
    methods: {
      deleteHouse() {
        this.$store.dispatch("deleteHouse", this.houseData._id)
      }
    }
  }
</script>

<style>
  .house {
    outline: 1px solid black;
  }
</style>