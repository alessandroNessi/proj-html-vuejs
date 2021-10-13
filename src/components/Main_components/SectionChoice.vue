<template>
    <div class="container-l">
        <div class="choice-card">
            <img src="../../assets/img/image_box_1-221x231.png" alt="instructor">
            <HPB :fontsize="14" :header="`Become an Instructor`" :paragraph="`Teach what you love. Masterstudy gives you the tools to create a course.`" :button="`START TEACHING`"/>
        </div>
        <div class="choice-card">
            <img src="../../assets/img/image_box_2-234x231.png" alt="business">
            <HPB :fontsize="14" :header="`Setup for Business`" :paragraph="`Get unlimited access to 2,500 of Udemy's top courses for your team.`" :button="`START TEACHING`"/>
        </div>
    </div>
</template>

<script>
import HPB from "./HPB.vue";
export default {
  name: "SectionChoice",
  components: {
    HPB,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
  .container-l{
    display: flex;
    justify-content: center;
    padding: 80px 50px;
    .choice-card{
      margin:0 20px;
      padding: 40px 20px;
      height: 300px;
      img{
        height: 100%;
        margin-right: 30px;
      }
      align-items: center;
      display: flex;
      border: 1px solid $grey300;
    }
  }
</style>