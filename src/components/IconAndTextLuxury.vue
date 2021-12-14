<template>
  <section class="iconBg">
    <div class="iconText">
      <div 
        class="middleIcons"
        v-for="(item, index) in middleIcons" :key="index" >
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
export default {
  name: "IconAndTextLuxury",

  data(){
    return {
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