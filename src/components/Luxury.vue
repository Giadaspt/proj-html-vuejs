<template>
  <div class="Luxury">
    <section class="LuxuryText" >
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
    </section>
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
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars.scss";
  @import "../assets/style/general.scss";
  @import "../assets/style/mixin.scss";
  @import "../assets/style/main.scss";
  @import "../assets/style/luxury.scss";
</style>