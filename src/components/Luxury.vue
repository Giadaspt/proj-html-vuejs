<template>
  <div class="middleMain">
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

    <section class="iconText">
      <div 
        v-for="(item, index) in middleIcons" :key="index"
        class="middleIcons">
        <i 
          :class="item.icon"
          class="icons">
        </i>
        <p> {{item.text}} </p>
      </div>
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

      middleIcons: [
        {
          icon: 'fas fa-sign-language',
          text: 'massages',
        },
        {
          icon: 'far fa-smile',
          text: 'therapy',
        },
        {
          icon: 'fas fa-heart',
          text: 'relaxing',
        },
        {
          icon: 'far fa-moon',
          text: 'meditation',
        },
        {
          icon: 'fas fa-snowflake',
          text: 'natural beauty',
        },
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