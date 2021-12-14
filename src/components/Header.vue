<template>
  <header >
    <section class="row d-flex">
      <ul>
        <li v-for="(menu, index) in navbar" :key="index">
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
export default {
  name: "Header",

  data(){
    return {
      
      navbar: [
        {
          icon: 'fas fa-home',
        },
        {
          icon: 'fab fa-pagelines',
          menu: "treatments",
          underMenu: "face & body",
        },
        {
          icon: 'fas fa-male',
          menu: "about",
          underMenu: "our team",
        },
        {
          logo: require('../assets/img/avada-spa-logo-new.png'),
        },
        {
          icon:'fas fa-heart',
          menu: "journal",
          underMenu: "tips & tricks",
        },
        {
          icon:'fas fa-bookmark',
          menu: "book now",
          underMenu: "special offers",
        },
        {
          icon:'fas fa-plus',
        },
      ],

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