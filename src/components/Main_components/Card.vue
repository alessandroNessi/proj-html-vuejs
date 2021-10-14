<template>
  <div class="frame">
    <div class="card">
      <div class="img_container">
        <img :src="require(`../../assets/img/${this.img}`)" :alt="this.title" />
        <div
          v-if="this.label !== false"
          :class="`label ${this.label.toLowerCase()}`"
        >
          {{ this.label }}
        </div>
        <div v-if="this.feature !== false" class="featured">FEATURED</div>
      </div>
      <div class="card_description">
        <p class="subtitle">{{ this.subtitle }}></p>
        <p class="title">{{ this.title }}</p>
        <div class="card_footer">
          <div class="rate">
            <p v-if="this.rating.type == 'time'">
              <i class="far fa-clock"></i> {{ this.rating.value }} hours
            </p>
            <p v-else>
              <img
                v-for="(element, index) in this.rating.value"
                :key="index"
                src="../../assets/img/starfull.svg"
                alt="valuestarfull"
              />{{ this.rating.value }}
            </p>
          </div>
          <div class="price">
            <p v-if="this.price.free">Free</p>
            <div v-else>
              <p v-if="this.price.discount !== ''" class="discount">
                {{ this.price.discount }}
              </p>
              <p>{{ this.price.value }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Banner",
  props: {
    img: String,
    subtitle: String,
    title: String,
    rating: Object,
    price: Object,
    label: String,
    feature: Boolean,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
$cardHeight: 350px;
.frame {
  height: $cardHeight;
  width: 100%;
  padding: 10px;
  .card {
    overflow: hidden;
    border: 1px solid $grey400;
    width: 100%;
    height: 100%;
    .img_container {
      height: 50%;
      position: relative;
      overflow: hidden;
      img {
        height: 100%;
      }
      .label,
      .featured {
        padding: 5px;
        font-size: 12px;
        color: white;
        position: absolute;
      }
      .label {
        top: 10px;
        right: 10px;
        border-radius: 5px;
      }
      .new {
        background-color: $green;
      }
      .hot {
        background-color: $red;
      }
      .special {
        background-color: $golden;
      }
      .featured {
        top: 10px;
        left: 10px;
        background-color: $golden;
        padding: 5px 50px;
        transform: rotate(-45deg) translate(-50px, -25px);
      }
    }
    .card_description {
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      height: 50%;
      padding: 10px;
      font-size: 14px;
      .subtitle {
        color: $grey700;
      }
      .title {
        color: $blue900;
      }
      .card_footer {
        border-top: 1px solid $grey400;
        color: $blue900;
        padding-top: 10px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        .price {
          font-weight: 600;
          .discount {
            color: $grey700;
            text-decoration: line-through;
          }
        }
      }
    }
  }
}
</style>
