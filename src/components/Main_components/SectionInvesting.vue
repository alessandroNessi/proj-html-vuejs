<template>
  <section class="investing">
    <div class="container-s">
      <div class="minibanner">
        <HPB
          class="banner_title"
          :fontsize="20"
          :header="`Start Investing in You`"
          :paragraph="`With over 1200 courses in 18 subjects, you're guaranteed to find something that's right for you`"
          :button="`JOIN FOR FREE`"
        />
        <div class="background_img">
          <img class="bgr" src="../../assets/img/base.png" alt="bgr" />
          <img
            class="img1"
            src="../../assets/img/book1.png"
            alt="img1 composed"
          />
          <img
            class="img2"
            src="../../assets/img/book2.png"
            alt="img2 composed"
          />
        </div>
      </div>
      <div class="goals">
        <Goal :icon="`fas fa-globe-africa`" :header="`Worldwide Recognize`" :paragraph="`Our online course certificates can be used around the wordl and also in most popular universities and companies.`" class="col-4" />
        <Goal :icon="`fas fa-desktop`" :header="`Mostly Online Learining (sd)`" :paragraph="`Masterstudy online certificates can be obtained in a range of specialized areas and typically take avout a year to complete.`" class="col-4" />
        <Goal :icon="`far fa-calendar-check`" :header="`Gradyate ub as kuttke as 1 Year`" :paragraph="`Online post-graduare certificates are a popilar way to develop your professional qualifications of Masterstudy`" class="col-4" />
      </div>
      <div class="courses">
          <Course :header="this.previewCourse.header" :paragraph="this.previewCourse.paragraph" :img="this.previewCourse.url" :preview="true" />
          <div class="lateral col-4">
              <Course v-for="(element, index) in this.lateralArray" :key="index" :header="element.header" :paragraph="element.paragraph" :preview="element.preview" :lateral="true" :img="element.url" />
          </div>
          <Course v-for="(element, index) in this.coursesArray" :key="index" :header="element.header" :paragraph="element.paragraph" :preview="element.preview" :img="element.url" />
      </div>
    </div>
  </section>
</template>

<script>
import HPB from "./HPB.vue";
import Goal from "./Goal.vue";
import Course from "./Course.vue";
export default {
  name: "SectionInvesting",
  components: {
    HPB,
    Goal,
    Course,
  },
  data(){
      return{
          previewCourse:{
                url:"cat_1-1540x750.jpg",
                header:"Software Developement",
                paragraph:"5",
                preview:false,
            },
          lateralArray:[
              {
                url:"cat_2-740x310.jpg",
                header:"Art",
                paragraph:"8",
                preview:false,
            },
            {
                url:"cat_3-740x310.jpg",
                header:"Material Design",
                paragraph:"5",
                preview:false,
            },
          ],
          coursesArray:[
            {
                url:"cat_5-740x310.jpg",
                header:"Music",
                paragraph:"5",
                preview:false,
            },
            {
                url:"cat_4-740x310.jpg",
                header:"Exercise",
                paragraph:"7",
                preview:false,
            },
            {
                url:"cat_6-740x310.jpg",
                header:"Photography",
                paragraph:"4",
                preview:false,
            },
          ],
      }
  }
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
.investing {
  padding: 50px 0;
  .minibanner {
    display: flex;
    align-items: center;
    height: 500px;
    .background_img {
      transform: translate(10%, 0);
      position: relative;
      .img1 {
        position: absolute;
        top: 25%;
        left: 60%;
      }
      .img2 {
        position: absolute;
        bottom: 10%;
        left: 35%;
      }
    }
  }
  .goals{
      display: flex;
      margin: 50px 0;
  }
  .courses{
      display: flex;
      flex-wrap: wrap;
  }
}
</style>
