<template>
  <div>
      <img :src="home.images[0]" width="200px"> <br/>
      {{home.title}} <br/>
      {{home.location.address}} <br/>
      {{home.location.city}} <br/>
      {{home.location.state}} <br/>
      {{home.guests}} / guests <br/>
      {{home.pricePerNight}} / Night <br/>
  </div>
</template>

<script>
  export default {
    props: {
      home: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>
