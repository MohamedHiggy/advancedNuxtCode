<template>
  <div class="container">
    <div v-for="home in homes" :key="home.objectID" class="card">
      <nuxt-link :to="`/home/${home.objectID}`" no-prefetch><HomeCard :home="home"></HomeCard></nuxt-link>
    </div>
  </div>
</template>

<script>
import homes from "@/data/homes";
export default {
  head() {
    return {
      title: "Homepage",
      meta: [{
        name: "description",
        content: "this is a homepage!",
        hid: "description"
      }]
    }
  },
  data() {
    return {
      homes: homes.slice(0,4)
    }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  justify-content: center;
  text-align: center;
  display: flex;
  flex-wrap: wrap;
}
.card {
  border: 1px solid red;
  padding: 15px;
  width: 33.333%;
  margin: 0 auto;
}
.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
