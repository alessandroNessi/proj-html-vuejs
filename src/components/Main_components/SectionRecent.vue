<template>
  <section class="recent">
    <div class="container-l">
      <h2>Recent Courses</h2>
      <ul class="link_list">
        <li v-for="(element, index) in this.linkArray" :key="index">
          <button class="rounded">{{ element }}</button>
        </li>
      </ul>
      <ul class="recent_list">
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
      <button class="rounded">SHOW ALL</button>
    </div>
  </section>
</template>

<script>
import Card from "./Card.vue";
import CardsArray from "./CardsArray.json";

export default {
  name: "SectionRecent",
  components: {
    Card,
  },
  data() {
    return {
      linkArray: [
        "All Categories",
        "Art",
        "Exercise",
        "Material Design",
        "Music",
        "Photography",
        "Software Development",
      ],
      cards: CardsArray,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
$stdMargin: 40px;
.container-l {
  padding-top: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  > * {
    margin-bottom: $stdMargin;
  }
  h2 {
    font-size: $stdFontSizeTitle;
    font-weight: $stdFontWeightTitle;
    color: $blue900;
  }
  .recent_list {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
  }
  .link_list {
    display: flex;
    li {
      padding: 0 8px;
      button {
        background-color: white;
        font-size: 14px;
        color: $blue400;
        &:hover {
          background-color: $grey300;
          color: $grey900;
        }
      }
    }
  }
}
</style>
