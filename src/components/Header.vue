<template>
  <header >
    <section class="row d-flex">
      <ul>
        <li v-for="(menu, index) in header" :key="index">
          <a 
            @click="[getIndex(index), item.active = !item.active]"
            :class="{active: index == indexArr}"
            href="#">
            <img :src="menu.logo" alt="">
            <i
              :class="menu.icon">
              </i>
            <h6>{{menu.menu}}</h6> 
            <p>{{menu.undermenu}}</p> 
          </a>
        </li>
      </ul>
    </section>
  </header>
</template>

<script>
import header from "../assets/data/header.js";

export default {
  name: "Header",

  data(){
    return {
      header, 
      indexArr: -1,
      active: false,
    }
  },
  methods: {
    
    getIndex(index){
      this.indexArr = index;
    }
  }
  
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";
@import "../assets/style/general.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/header.scss";

</style>