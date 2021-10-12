<template>
  <section class="recent">
    <div class="container-l">
      <h2>Recent Courses</h2>
      <ul class="link_list">
        <li v-for="(element, index) in this.linkArray" :key="index"><button class="rounded">{{element}}</button></li>
      </ul>
      <ul class="recent_list">
        <li class="col-2"><Card/></li>
      </ul>
    </div>
  </section>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "SectionRecent",
  components: {
    Card,
  },
  data() {
    return {
      linkArray:[
        "All Categories",
        "Art",
        "Exercise",
        "Material Design",
        "Music",
        "Photography",
        "Software Development"
      ],
      cards: [
        {
          img:"photo-1461749280684-dccba630e2f6-544x322.jpeg",
          subtitle: "Apache>",
          title: "Web Coding and Apache Basics",
          rating:{
            type: "time",
            value: 6,
          },
          prize:{
            free:true,
          },
          label:false,
          feature: false,
        },
        {
          img:"cat_2-544x322.jpg",
          subtitle: "Art>",
          title: "Real Things Art Painting by Jason Ni",
          rating:{
            type: "time",
            value: 6,
          },
          prize:{
            free:false,
            discaunt:"$60",
            price:"$45"
          },
          label:"NEW",
          feature: true,
        },
      ],
    }
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
  $stdMargin: 30px;
  .container-l{
    padding-top: 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    >*{
      margin-bottom: $stdMargin;
    }
    h2{
      font-size: $stdFontSizeTitle;
      font-weight: $stdFontWeightTitle;
      color: $blue900;
    }
    .recent_list{
      width: 100%;
    }
    .link_list{
      display: flex;
      li{
        padding:0 8px;
        button{
          background-color: white;
          font-size: 14px;
          color: $blue400;
          &:hover{
            background-color: $grey300;
            color: $grey900;
          }
        }
      }
    }
  }
</style>
