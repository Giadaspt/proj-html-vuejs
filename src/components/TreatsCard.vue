<template>
  <div class="col-3 ">
    <div class=" preview">
      <img :src="preview" alt="">
      <div class="text">
        <h5> {{title}} </h5>
        <div class="divider"></div>
        <p> {{subTitle}} </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TreatsCard",

  props: {
    preview: String,
    title: String,
    subTitle: String,
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars.scss";
@import "../assets/style/general.scss";
@import "../assets/style/mixin.scss";
@import "../assets/style/treatsCard.scss";

</style>