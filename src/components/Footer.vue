<template>
  <footer class="d-flex">
    <div class="logoImg">
      <img :src="footerDetails.image" alt="">
    </div>
    <div class="footerText">
      <p> {{footerDetails.text}} </p>
    </div>
    <div 
      class="footerIcons"
      v-for="(item, index) in icons" :key="index">
      <a href="#">
        <i 
        :class="item"></i>
      </a>
    </div>
    <div class="goUp">
      <a href="#">
        <i 
        :class="footerDetails.chevron"
        class="chevron"></i>
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",

  data(){
    return {
      footerDetails: {
        image: require("../assets/img/avada-spa-logo-new.png"),
        text: "copyright 2012 - 2020' | avada theme | all rights receerved | powered by giada",
        chevron: 'fas fa-chevron-up',
      },

      icons: [
        "fab fa-facebook-f",
        "fab fa-twitter",
        "fab fa-instagram",
        "fab fa-youtube",
      ],

      indexIcon: -1,
    }
  },

}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars.scss";
  @import "../assets/style/general.scss";
  @import "../assets/style/mixin.scss";
  @import "../assets/style/footer.scss";
    
</style>