<template>
  <section class="row faceBodyTreatments">
    <div class="picAndText">
      <div class="imageBath">
        <img :src="image" alt="">
      </div>
      <div class="faceBodyRight">
        <h2> {{faceAndBody.title}} </h2>
        <p> {{faceAndBody.text}} </p>

        <div 
          class="infoBox"
          v-for="(item, index) in infoBox" :key="index">
          <i 
            @click="[iconChange(index), item.show = !item.show]"
            :class="item.iconPlus">
          </i>
          <h6> {{item.title}} </h6>
          <p> {{item.text}} </p>
        </div>
        <button class="btn btnFaceBody"> book an appointment </button>
      </div>

    </div>
    <div class="bG">
      <h4>{{treats}}</h4>
      <img :src="imageBg" alt="">
    </div>
  </section>
</template>

<script>
export default {
  name:"FaceAndBody",

  data(){
    return {
      image: require('../assets/img/face_and_body_treatments-new-400x581.jpg'),

      faceAndBody: {
        title: 'face & body treatments',
        text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae officiis expedita minus suscipit voluptatibus ullam dolorum. Soluta esse nobis voluptate',
      },

      infoBox: [
        {
          title: 'oil massage',
          iconPlus:'fas fa-plus-square',
          iconMinus:'fas fa-minus-square',
          info: '$62 For 2 hours - Lorem ipsum dolor',
        },
        {
          title: 'manicure',
          iconPlus:'fas fa-plus-square',
          iconMinus:'fas fa-minus-square',
          info: '$62 For 2 hours - Lorem ipsum dolor',
        },
        {
          title: 'aromatherapy',
          iconPlus:'fas fa-plus-square',
          iconMinus:'fas fa-minus-square',
          info: '$62 For 2 hours - Lorem ipsum dolor',
        },
      ],

      imageBg: require('../assets/img/ptb_cta-new.jpg'),
      treats: 'our treatments',
      show: false,
      indexArr: -1,
    }
  },

  methods: {
    getIndex(index){
      this.indexArr = index ;
    },

    iconChange(){
      if (this.show == true) {
        return this.infoBox[this.getIndex].iconPlus
      }
      return this.infoBox[this.getIndex].iconMinus
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