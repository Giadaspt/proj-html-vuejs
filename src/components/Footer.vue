<template>
  <footer>
    <img :src="image" alt="">
  </footer>
</template>

<script>
export default {
  name: "Footer",

  data(){
    return {
      image: require("../assets/img/avada-spa-logo-new.png")
    }
  }
}
</script>

<style lang="scss" scoped>

</style>