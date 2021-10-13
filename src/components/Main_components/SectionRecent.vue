<template>
  <section class="recent">
    <div class="container-l">
      <h2>Recent Courses</h2>
      <ul class="link_list">
        <li v-for="(element, index) in this.linkArray" :key="index"><button class="rounded">{{element}}</button></li>
      </ul>
      <ul class="recent_list">
        <li v-for="(element,index) in this.cards" :key="index" class="col-2"><Card :img="element.img" :subtitle="element.subtitle" :title="element.title" :rating="element.rating" :price="element.price" :label="element.label" :feature="element.feature"  /></li>
      </ul>
      <button class="rounded">SHOW ALL</button>
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
        },
        {
          img:"photo-1475452779376-caebfb988090-544x322.jpeg",
          subtitle: "Bicycling",
          title: "Road Bike Manual or How to Be a Champion",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:false,
            discount:"",
            value:"$20"
          },
          label: false,
          feature: false,
        },
        {
          img:"cristian-grecu-762012-unsplash-min-scaled-544x322.jpg",
          subtitle: "Documentary",
          title: "How to Make Beautiful Landscae photos?",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:false,
            discount:"",
            value:"$60"
          },
          label: false,
          feature: false,
        },
        {
          img:"landscape-544x322.jpg",
          subtitle: "Art",
          title: "Let's paint Ban Gogh's Starry Night",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:false,
            discount:"",
            value:"$79"
          },
          label: false,
          feature: false,
        },
        {
          img:"12345-1-544x322.png",
          subtitle: "Nvidia",
          title: "Nvidia and UE4 Technologies Practice",
          rating:{
            type: "star",
            value: 5,
          },
          price:{
            free:true,
          },
          label: "SPECIAL",
          feature: false,
        },
        {
          img:"jakob-owens-198234-unsplash-min-1-544x322.png",
          subtitle: "Art",
          title: "How to Work with Legendary RED camera?",
          rating:{
            type: "time",
            value: 6,
          },
          price:{
            free:true,
          },
          label: "SPECIAL",
          feature: false,
        },
        {
          img:"promo_tf-544x322.jpg",
          subtitle: "Software Development",
          title: "MasterStudy Mobile LMS App",
          rating:{
            type: "time",
            value: 2,
          },
          price:{
            free:true,
          },
          label: false,
          feature: false,
        },
      ],
    }
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
  $stdMargin: 40px;
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
      display: flex;
      flex-wrap: wrap;
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
