<template>
  <section class="proud">
    <div class="first container-l">
      <ProudTitleSub
        :fontsize="'20'"
        :header="`We are Proud`"
        :paragraph="`Certificate courses are instructed by highly educated and qualified instructors who hold doctoral and master's level degrees.`"
      />
      <div class="recap">
        <div class="floating">
          <ProudTitleSub
            class="subcategories"
            v-for="(element, index) in this.proudArray"
            :key="index"
            :fontsize="'25'"
            :header="element.header"
            :paragraph="element.paragraph"
          />
        </div>
        <img src="../../assets/img/we_proud.png" alt="" />
      </div>
      <div class="newsletter">
        <div class="container-s">
          <div class="newsletter_element">
            <h4>Subscribe our newsletter</h4>
            <p>
              There are many bariations of passages of Lorem Ipsum avaible, but
              the majority have suffered alteration in some fore, by injected
              humor or randomised words
            </p>
          </div>
          <div class="newsletter_element">
            <h4>YOUR E-MAIL ADDRESS</h4>
            <div class="newsletter_subscribe">
              <input type="mail" placeholder="Enter your E-mail" /><button>
                SUBSCRIBE
              </button>
            </div>
          </div>
        </div>
      </div>
      <div class="popular_courses">
        <ProudTitleSub
          :fontsize="'20'"
          :header="`Popular courses`"
          :paragraph="`Discover our most popular courses for self learning`"
        />
      </div>
      <ul class="popular_list">
        <li v-for="(element, index) in this.cards" :key="index" class="col-2">
          <Card
            :img="element.img"
            :subtitle="element.subtitle"
            :title="element.title"
            :rating="element.rating"
            :price="element.price"
            :label="element.label"
            :feature="element.feature"
          />
        </li>
      </ul>
      <div class="switch_page">
        <i @click="prevCourse()" class="fas fa-chevron-left"></i>
        <i @click="nextCourse()" class="fas fa-chevron-right"></i>
      </div>
    </div>
  </section>
</template>

<script>
import Card from "./Card.vue";
import ProudTitleSub from "./ProudTitleSub.vue";
import CardsArray from "./CardsArray.json";

export default {
  name: "SectionProud",
  components: {
    Card,
    ProudTitleSub,
  },
  data() {
    return {
      proudArray: [
        {
          header: "2000",
          paragraph: "STUDENTS",
        },
        {
          header: "950",
          paragraph: "COURSES",
        },
        {
          header: "1600",
          paragraph: "HOURS VIDEO",
        },
        {
          header: "150",
          paragraph: "COUNTRIES REACHED",
        },
      ],
      cards: [],
      CardsArray: CardsArray,
      i: 0,
    };
  },
  methods: {
    nextCourse() {
      if (this.i + 1 < this.CardsArray.length) {
        this.cards = [];
        let temp = this.i + 6;
        while (this.i < temp) {
          this.cards.push(this.CardsArray[this.i]);
          this.i++;
        }
      }
    },
    prevCourse() {
      if (this.i > 11) {
        this.cards = [];
        let temp = this.i - 6;
        this.i -= 12;
        while (this.i < temp) {
          this.cards.push(this.CardsArray[this.i]);
          this.i++;
        }
      }
    },
  },
  mounted() {
    this.nextCourse();
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
$stdMargin: 20px;
.container-l {
  margin-top: $stdMargin;
  padding-top: calc($stdMargin * 4);
  background-color: $grey200;
  display: flex;
  flex-direction: column;
  //newsletter
  .newsletter {
    background-color: $green;
    padding: calc($stdMargin * 2) 0;
    width: 100%;
    .container-s {
      display: flex;
      .newsletter_element {
        width: 50%;
        padding-right: 60px;
        .newsletter_subscribe {
          input {
            width: 50%;
            padding-left: 20px;
          }
        }
        &:last-child {
          padding: 0;
        }
        color: white;
        h4 {
          font-weight: 600;
          margin-bottom: $stdMargin;
        }
        p {
          font-size: 14px;
        }
      }
    }
  }
  //recap
  .recap {
    height: 450px;
    position: relative;
    display: flex;
    flex-direction: column-reverse;
    img {
      width: 100%;
    }
    .floating {
      position: absolute;
      display: flex;
      justify-content: center;
      top: calc($stdMargin * 3);
      width: 100%;
      .subcategories {
        border-right: 1px solid $grey400;
        padding: 0 30px;
        &:last-child {
          border-right: 0px;
        }
      }
    }
  }
  //popular
  .popular_courses {
    padding-top: calc($stdMargin * 4);
  }
  .popular_list {
    margin: calc($stdMargin * 3) 0 calc($stdMargin * 2) 0;
    width: 100%;
    display: flex;
    flex-wrap: wrap;
  }
  h2 {
    font-size: $stdFontSizeTitle;
    font-weight: $stdFontWeightTitle;
    color: $blue900;
    padding-bottom: $stdMargin;
  }
  .headersub {
    max-width: 800px;
    text-align: center;
    line-height: 25px;
  }
  .switch_page {
    padding-bottom: calc($stdMargin * 3);
    .fas {
      $size: 40px;
      background-color: white;
      width: $size;
      text-align: center;
      line-height: $size;
      border: 1px solid $grey400;
      color: $grey400;
      &:hover {
        background-color: $gullgray;
        color: white;
        transition: 0.1s;
      }
    }
  }
  .footer {
    display: flex;
  }
}
</style>
