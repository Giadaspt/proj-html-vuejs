<template>
  <header >
    <section class="row d-flex">
      <ul>
        <li>
          <a href="#">
            <i class="fas fa-home"></i>
          </a>
        </li>
        <li> 
          <a href="#">
            <i class="fab fa-pagelines"></i>
            <h6>treatments</h6> 
            <p>face & body</p> 
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fas fa-male"></i>
            <h6>about</h6>
            <p>our team</p>
          </a>
        </li>
        <li class="logo">
          <img :src="logo" alt="">
        </li>
        <li>
          <a href="#">
            <i class="fas fa-heart"></i>
            <h6>journal</h6>
            <p>tips & tricks</p>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fas fa-bookmark"></i>
            <h6>book now</h6>
            <p>special offers</p>
          </a>
        </li>
        <li>
          <a href="#">
            <i class="fas fa-plus"></i>
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
      logo: require('../assets/img/avada-spa-logo-new.png'),
      navbar: [
        {
          icon: "home-solid.svg",
          menu: "treatments",
          underMenu: "face & body",
        },
        {
          menu: "about",
          underMenu: "our team",
        },
        {
          menu: "journal",
          underMenu: "tips & tricks",
        },
        {
          menu: "book now",
          underMenu: "special offers",
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/general.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/header.scss";

  header{
    background-color: aquamarine;
  }
</style>