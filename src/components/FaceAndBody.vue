<template>
  <section class="row faceBodyTreatments">
    <div class="picAndText">
      <div class="imageBath">
        <img :src="image" alt="">
      </div>
      <div class="faceBodyRight">
        <h2> {{bodyCare.title}} </h2>
        <p class="pText"> {{bodyCare.text}} </p>

        <div 
          class="infoBox"
          v-for="(item, index) in faceAndBody" :key="index">
          <div class="nameInfo">
            <!-- al click appare il costo e cambia l'icona -->
            <i 
              @click="show = !show , getIndex(index)"
              :class="[index == indexIcon ? item.iconMinus : item.iconPlus]">
            </i>
            <h6> {{item.titleInfo}} </h6>
          </div>
          <p 
          v-if="show == true && index == indexIcon"
          :class="{visible: show == true}"
          class="hide"> {{item.info}} </p>
        </div>
        <button class="btn btnFaceBody"> {{button}} </button>
      </div>
    </div>
    
  </section>
</template>

<script>
import faceAndBody from "../assets/data/faceAndBody.js";

export default {
  name:"FaceAndBody",

  data(){
    return {
      faceAndBody,

      image: require('../assets/img/face_and_body_treatments-new-400x581.jpg'),

      bodyCare: {
        title: 'face & body treatments',
        text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae officiis expedita minus suscipit voluptatibus ullam dolorum. Soluta esse nobis voluptate',
      },

      button: 'book an appointment',

      show: false,
      indexIcon: -1,
    }
  },

  methods: {
    getIndex(index){
      this.indexIcon = index;
      console.log(index);
      console.log(this.indexIcon);
    },
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars.scss";
  @import "../assets/style/general.scss";
  @import "../assets/style/mixin.scss";
  @import "../assets/style/faceBodyTreatments.scss";
  @import "../assets/style/main.scss";
</style>