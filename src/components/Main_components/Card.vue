<template>
  <div class="frame">
    <div class="card">
      <div class="img_container">
        <img src="../../assets/img/cat_2-370x155.jpg" alt="">
        <div class="label">NEW</div>
        <div class="featured">FEATURED</div>
      </div>
      <div class="card_description">
        <p class="subtitle">Apache></p>
        <p class="title">Web Coding and Apache Basics</p>
        <div class="card_footer">
          <div class="rate">
            <p><i class="fas fa-clock"></i> 6 hours</p>
            <!-- <p><img src="../../assets/img/starfull.svg" alt=""></p> -->
          </div>
          <div class="price">
            <p>Free</p>
            <!-- <div>
              <p class="discount">$59</p>
              <p>$49</p>  
            </div> -->
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
    img:String,
    subtitle:String,
    title:String,
    rating: Object,
    prize: Object,
    label: String,
    feature: Boolean
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
  @import "../../assets/style/common.scss";
  $cardHeight : 350px;
  .frame{
    height: $cardHeight;
    width: 100%;
    padding: 10px;
    .card{
      overflow: hidden;
      border: 1px solid $grey300;
      width: 100%;
      height: 100%;
      .img_container{
        height: 50%;
        position: relative;
        overflow: hidden;
        .label, .featured{
          padding: 5px;
          font-size: 12px;
          color: white;
          position: absolute;
        }
        .label{
          top:10px;
          right: 10px;
          border-radius: 5px;
          background-color: red;
        }
        .featured{
          top: 10px;
          left: 10px;
          background-color: $golden;
          padding: 5px 50px;
          transform: rotate(-45deg) translate(-50px, -25px);
        }
      }
      .card_description{
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        height: 50%;
        padding: 10px;
        font-size: 14px;
        .subtitle{
          color: $grey700;
        }
        .title{
          color: $blue900;
        }
        .card_footer{
          border-top: 1px solid $grey300;
          color: $blue900;
          padding-top: 10px;
          display: flex;
          align-items: center;
          justify-content: space-between;
          .price{
            font-weight: 600;
            .discount{
              color: $grey700;
              text-decoration: line-through;
            }
          }
        }
      }
    }
  }
</style>
