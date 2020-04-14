<template>
  <div class="create-house border col-12">
    <form @submit.prevent="createHouse()">
      <div class="form-group">
        <label for="bedrooms">Beds</label>
        <input type="number" name="bedrooms" id="" class="form-control" placeholder="enter Bedrooms..." aria-describedby="helpId"
          v-model="newHouse.bedrooms" required>
      </div>
      <div class="form-group">
        <label for="bathrooms">Baths</label>
        <input type="number" name="bathrooms" id="" class="form-control" placeholder="enter Bathrooms..."
          aria-describedby="helpId" v-model="newHouse.bathrooms" required>
      </div>
      <div class="form-group">
        <label for="year">Year</label>
        <input type="number" name="year" id="" class="form-control" placeholder="enter Year..."
          aria-describedby="helpId" v-model="newHouse.year" required>
      </div>
      <div class="form-group">
        <label for="price">Price</label>
        <input type="number" name="price" id="" class="form-control" placeholder="enter Price..."
          aria-describedby="helpId" v-model="newHouse.price" required>
      </div>
      <div class="form-group">
        <label for="img">Image</label>
        <input type="text" name="img" id="" class="form-control" placeholder="enter Img URL..." aria-describedby="helpId"
          v-model="newHouse.imgUrl" required>
      </div>
      <button type="submit" class="btn btn-success"> Add House</button>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'create-house',
    data() {
      return {
        newHouse: {}
      }
    },
    methods: {
      createHouse() {
        this.$store.dispatch('createHouse', this.newHouse)
        this.newHouse = {}
      }
    }
  }
</script>

<style>
  .create-house {
    outline: 1px solid black;
  }
</style>