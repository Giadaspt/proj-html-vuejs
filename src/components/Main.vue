<template>
  <main >
    <div class="centerTextButton">
      <h4> give yourself permission </h4>
      <h2> relax, revite & renjuvinate </h2>
      <button class="btn"> explore treatments </button>
    </div>
    <img :src="image" alt=""> 
  </main>
</template>

<script>
export default {
  name: "Main",

  data(){
    return {
      image: require('../assets/img/avada-spa-slider-image-1-new.jpg'),
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";
@import "../assets/style/general.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/main.scss";


</style>