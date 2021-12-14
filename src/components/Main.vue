<template>
  <main>
    <section class="jumbotron"> 
      <div class="heroArea ">
        <h4> {{text.overtitle}} </h4>
        <h2> {{text.title}} </h2>
        <button class="btn btnFirst"> explore treatments </button>
      </div>
      <img :src="image" alt=""> 
    </section>

    <Luxury/>
    <IconAndTextLuxury/>
    <FaceAndBody/>

    <!-- our treatment part, just image and title before the cards -->
    <div class="bG">
      <h4>{{greyBgWithImg.treats}}</h4>
      <img :src="greyBgWithImg.imageBg" alt="">
    </div>

    <TreatsCard
    v-for="(item, index) in  treatsCard" :key="index"
    :preview="item.imgPreview"
    :title="item.title"
    :subTitle="item.subTitle"
    />

    <!-- soon after the cards -->
    <div class="parfumImg">
      <img :src="imageFinal" alt="">
      <div class="cit">
        <p> "{{lorem}}"... </p>
        <h5> {{signature}} </h5>
      </div>
    </div>

    <!-- our treatment part, just image and title after the cards -->
    <div class="bGsecond">
      
    </div>
  </main>
</template>

<script>
import Luxury from "./Luxury.vue"
import IconAndTextLuxury from "./IconAndTextLuxury.vue"
import FaceAndBody from "./FaceAndBody.vue"
import TreatsCard from "./TreatsCard.vue"

import treatsCard from "../assets/data/treatsCard.js";

export default {
  name: "Main",

  components: {
    Luxury,
    IconAndTextLuxury,
    FaceAndBody,
    TreatsCard,
  },

  data(){
    return {
      treatsCard,

      image: require('../assets/img/avada-spa-slider-image-1-new.jpg'),

      text:{
        overtitle: 'Give yourself permission',
        title: 'relax, revite & renjuvinate',
      },

      greyBgWithImg: {
        imageBg: require('../assets/img/ptb_cta-new.jpg'),
        treats: 'our treatments',
      },

      imageFinal: require("../assets/img/Home-quota-new.jpg"),
      lorem: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga aspernatur accusantium sed voluptates eos ullam repudiandae, molestiae placeat repellat iure.",
      signature: 'fireda friedson, massuese',
    

    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";
@import "../assets/style/general.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/main.scss";
@import "../assets/style/faceBodyTreatments.scss";


</style>