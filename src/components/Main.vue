<template>
  <main>
    <div class="centerTextButton">
      <h4> {{text.overtitle}} </h4>
      <h2> {{text.title}} </h2>
      <button class="btn btnFirst"> explore treatments </button>
    </div>
    <img :src="image" alt=""> 

    <LuxuryText/>
  </main>
</template>

<script>
import LuxuryText from "./LuxuryText.vue"

export default {
  name: "Main",

  components: {
    LuxuryText,
  },

  data(){
    return {
      image: require('../assets/img/avada-spa-slider-image-1-new.jpg'),

      text:{
        overtitle: 'give yourself permission',
        title: 'relax, revite & renjuvinate',
      }
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