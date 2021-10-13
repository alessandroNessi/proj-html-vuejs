<template>
  <div class="cont">
    <h2 :style="`font-size:${this.fontsize * 2.75}px`">{{ this.header }}</h2>
    <p :style="`font-size:${this.fontsize}px`">{{ this.paragraph }}</p>
  </div>
</template>

<script>
export default {
  name: "ProudTitleSub",
  props: {
    header: String,
    paragraph: String,
    fontsize: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
$distance: 30px;
$stdMargin: 20px;
.cont {
  color: $blue900;
  h2 {
    font-weight: $stdFontWeightTitle;
    padding-bottom: $stdMargin;
    text-align: center;
  }
  p {
    max-width: 900px;
    text-align: center;
    line-height: 25px;
  }
}
</style>