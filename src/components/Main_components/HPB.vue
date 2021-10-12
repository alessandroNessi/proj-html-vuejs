<template>
  <div class="hpb">
    <h2 :style="`font-size:${this.fontsize * 2.75}px`">{{ this.header }}</h2>
    <p :style="`font-size:${this.fontsize}px`">{{ this.paragraph }}</p>
    <button class="rounded">{{ this.button }}</button>
  </div>
</template>

<script>
export default {
  name: "HPB",
  props: {
    header: String,
    paragraph: String,
    button: String,
    fontsize: String,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
$distance: 30px;
.hpb {
  color: $blue900;
  h2 {
    font-weight: 400;
    margin-bottom: $distance;
  }
  p {
    margin-bottom: $distance;
  }
}
</style>
