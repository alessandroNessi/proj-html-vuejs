<template>
  <section class="proud">
    <div class="first container-l">
      <ProudTitleSub :fontsize="'20'" :header="`We are Proud`" :paragraph="`Certificate courses are instructed by highly educated and qualified instructors who hold doctoral and master's level degrees.`"/>
      <div class="recap">
        <div class="floating">
          <ProudTitleSub class="subcategories" v-for="(element, index) in this.proudArray" :key="index" :fontsize="'25'" :header="element.header" :paragraph="element.paragraph"/>
        </div>
        <img src="../../assets/img/we_proud.png" alt="">
      </div>
      <!-- <ul class="recent_list">
        <li v-for="(element,index) in this.cards" :key="index" class="col-2"><Card :img="element.img" :subtitle="element.subtitle" :title="element.title" :rating="element.rating" :price="element.price" :label="element.label" :feature="element.feature"  /></li>
      </ul> -->
    </div>
  </section>
</template>

<script>
// import Card from "./Card.vue";
import ProudTitleSub from "./ProudTitleSub.vue";

export default {
  name: "SectionProud",
  components: {
    // Card,
    ProudTitleSub,
  },
  data() {
    return {
      proudArray:[
        {
          header:"2000",
          paragraph:"STUDENTS",
        },
        {
          header:"950",
          paragraph:"COURSES",
        },
        {
          header:"1600",
          paragraph:"HOURS VIDEO",
        },
        {
          header:"150",
          paragraph:"COUNTRIES REACHED",
        },
      ],
      cards: [
        {
          img:"photo-1461749280684-dccba630e2f6-544x322.jpeg",
          subtitle: "Apache",
          title: "Web Coding and Apache Basics",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:true,
          },
          label:false,
          feature: false,
        },
        {
          img:"cat_2-544x322.jpg",
          subtitle: "Art",
          title: "Real Things Art Painting by Jason Ni",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:false,
            discount:"$60",
            value:"$45"
          },
          label:"NEW",
          feature: true,
        },
        {
          img:"course-preview-544x322.jpg",
          subtitle: "Software Development",
          title: "Basics of Masterstudy",
          rating:{
            type: "star",
            value: 5,
          },
          price:{
            free:true,
          },
          label:"HOT",
          feature: false,
        },
        {
          img:"photo-1496307042754-b4aa456c4a2d-544x322.jpeg",
          subtitle: "Electronic",
          title: "How to be a DJ? Make Electronic Music",
          rating:{
            type: "star",
            value: 5,
          },
          price:{
            free:false,
            discount:"$59",
            value:"$49"
          },
          label:"SPECIAL",
          feature: false,
        },
        {
          img:"photo-1416339134316-0e91dc9ded92-scaled-544x322.jpeg",
          subtitle: "Comunication",
          title: "Design Instruments for Communication",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:false,
            discount:"",
            value:""
          },
          label: false,
          feature: false,
        },
        {
          img:"cathryn-lavery-67852-unsplash-544x322.jpg",
          subtitle: "Art",
          title: "Make Your Concepr Right and Beautiful",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:false,
            discount:"",
            value:"$70"
          },
          label: false,
          feature: false,
        }
      ],
    }
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
  $stdMargin: 20px;
  .container-l{
    margin-top: $stdMargin;
    padding-top: calc($stdMargin * 4);
    background-color: $grey200;
    display: flex;
    flex-direction: column;
    .recap{
      height: 450px;
      position: relative;
      display: flex;
      flex-direction: column-reverse;
      img{
        width: 100%;
      }
      .floating{
        position: absolute;
        display: flex;
        justify-content: center;
        top: calc($stdMargin * 3);
        width: 100%;
        .subcategories{
          border-right: 1px solid $grey400;
          padding: 0 30px;
          &:last-child{
            border-right: 0px;
          }
        }
      }
    }
    h2{
      font-size: $stdFontSizeTitle;
      font-weight: $stdFontWeightTitle;
      color: $blue900;
      padding-bottom: $stdMargin;
    }
    .headersub{
      max-width: 800px;
      text-align: center;
      line-height: 25px;
    }
  }
</style>
