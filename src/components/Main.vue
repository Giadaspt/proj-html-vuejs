<template>
  <main>
    <section class="jumbotron"> 
      <div class="heroArea ">
        <h4> {{jumbo.overtitle}} </h4>
        <h2> {{jumbo.title}} </h2>
        <button class="btn btnFirst"> {{jumbo.button}} </button>
      </div>
      <!-- two little squares on right side of jumbotron -->
      <div class="demosOnSale">
        <div class="demos">
          <img :src="demosAndSale.imageDemos" :alt="demosAndSale.demos">
          <p> {{demosAndSale.demo}} </p>
        </div>
        <div class="onSale">
          <img :src="demosAndSale.imageCost" :alt="demosAndSale.onSale">
          <p> {{demosAndSale.onSale}} </p>
        </div>
      </div>
      <img :src="jumbo.image" alt=""> 
    </section>

    <Luxury/>
    <IconAndTextLuxury/>
    <FaceAndBody/>

    <!-- our treatment part, just image and title before the cards -->
    <div class="bG bGfirst">
      <h4>{{treatment.treats}}</h4>
      <img :src="treatment.imageBg" alt="">
    </div>

    <TreatsCard
    v-for="(item, index) in  treatsCard" :key="index"
    :preview="item.imgPreview"
    :title="item.title"
    :subTitle="item.subTitle"
    />

    <!-- soon after the cards -->
    <div class="parfumImg">
      <div class="citation">
        <p> "{{citation.lorem}}..." </p>
        <h6> {{citation.signature}} </h6>
      </div>
      <img :src="citation.imageFinal" alt="">
    </div>

    <!-- our treatment part, just image and title after the cards -->
    <div class="bG bGsecond">
      <img :src="treatment.imageBg" alt="">
      <div class="offer">
        <div class="discount">
          <h4> {{treatment.off}}  </h4>
          <p> {{treatment.specialOffer}} </p>
        </div>
        <div class="offerText">
          <h4> {{treatment.takeTime}} </h4>
          <p> {{treatment.textOffer}} </p>
        </div>
        <button class="btn butn"> {{treatment.butn}} </button>
      </div>
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
      jumbo: {
        image: require('../assets/img/avada-spa-slider-image-1-new.jpg'),
        overtitle: 'Give yourself permission',
        title: 'relax, revite & renjuvinate',
        button: 'explore treatments',
      },

      treatment: {
        imageBg: require('../assets/img/ptb_cta-new.jpg'),
        treats: 'our treatments',
        off: '25%',
        specialOffer: 'special offer',
        takeTime: 'Take some time. Treat yourself. You deserve it.',
        textOffer: 'Book a treatment this month and receive 25% off on all further treatments.',
        butn: 'book now',
      },

      citation: {
        imageFinal: require("../assets/img/Home-quota-new.jpg"),
        lorem: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga aspernatur accusantium sed voluptates eos ullam repudiandae, molestiae placeat repellat iure.Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga aspernatur accusantium sed voluptates ",
        signature: 'frieda friedson, massuese',
      },

      demosAndSale: {
        imageDemos: require("../assets/img/iconaCheNonRiuscivoATrovare.png"),
        demo: 'demos',
        imageCost: require("../assets/img/cost.png"),
        onSale: 'on sale',
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
  @import "../assets/style/luxury.scss";
  @import "../assets/style/iconAndTextLuxury.scss";
  @import "../assets/style/faceBodyTreatments.scss";


</style>