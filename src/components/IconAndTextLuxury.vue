<template>
  <section class="iconBg">
    <div class="iconText">
      <div 
        class="middleIcons"
        v-for="(item, index) in iconAndTextLuxury" :key="index" >
        <i 
          :class="item.icon"
          class="icons">
        </i>
        <p> {{item.text}} </p>
      </div>
    </div>
    
  </section>
</template>

<script>
import iconAndTextLuxury from "../assets/data/iconAndTextLuxury.js";

export default {
  name: "IconAndTextLuxury",

  data(){
    return {
      iconAndTextLuxury,
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
</style>