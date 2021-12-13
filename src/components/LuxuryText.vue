<template>
  <div class="LuxuryText ">

    <h2> {{text.title}} </h2> 
    <i class="leaf"
      :class="text.icon">
    </i>

    <h5 class="topText">
      {{text.topText}}
    </h5>

    <div class="line"></div>

    <h6 class="afterLine">
      {{text.afterLine}}
    </h6>

    <button class="btn btnSecond"> our approach </button>

    <div class="middleIcons">
      <i class="fas fa-sign-language"></i>
      <i class="far fa-smile"></i>
      <i class="fas fa-heart"></i>
      <i class="far fa-moon"></i>
      <i class="fas fa-snowflake"></i>
    </div>
  </div>
</template>

<script>


export default {
  name: "LuxuryText",

  data(){
    return {
      text: {
        title: 'luxury spa experience',
        icon: 'fab fa-envira',
        topText: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Minima accusantium exercitationem, voluptates ',
        afterLine: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur quisquam aspernatur veritatis voluptatem non qui, cum dignissimos architecto assumenda magni obcaecati',
      },
      middleIcons: [
        {
          icon: 'fas fa-sign-language',
        }
      ]
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