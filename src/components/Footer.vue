<template>
  <footer ref="footer">
    <div class="container-s">
      <div class="footer_card">
        <h2>About</h2>
        <p><a class="link" href="#">Masterstudy</a> is Education WordPress theme featured by Learning Management System (LMS) for online education.</p>
        <p>Developed by <a href="#" class="link">StylemyxThemes</a></p>
        <p class="comments"><i class="fab fa-facebook"></i><i class="fab fa-twitter"></i><i class="fab fa-instagram"></i></p>
      </div>
      <div class="footer_card">
        <h2>About</h2>
        <p><a class="link" href="#">Masterstudy</a> is Education WordPress theme featured by Learning Management System (LMS) for online education.</p>
        <p>Developed by <a href="#" class="link">StylemyxThemes</a></p>
        <p class="comments"><i class="fab fa-facebook"></i><i class="fab fa-twitter"></i><i class="fab fa-instagram"></i></p>
      </div>
      <div class="footer_card">
        <h2>About</h2>
        <p><a class="link" href="#">Masterstudy</a> is Education WordPress theme featured by Learning Management System (LMS) for online education.</p>
        <p>Developed by <a href="#" class="link">StylemyxThemes</a></p>
        <p class="comments"><i class="fab fa-facebook"></i><i class="fab fa-twitter"></i><i class="fab fa-instagram"></i></p>
      </div>
      <div class="footer_card">
        <h2>About</h2>
        <p><a class="link" href="#">Masterstudy</a> is Education WordPress theme featured by Learning Management System (LMS) for online education.</p>
        <p>Developed by <a href="#" class="link">StylemyxThemes</a></p>
        <p class="comments"><i class="fab fa-facebook"></i><i class="fab fa-twitter"></i><i class="fab fa-instagram"></i></p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {
  },
  data() {
    return {};
  },
  methods: {},
  mounted() {
  },
};
</script>

<style lang="scss" scoped>
$footerFontSize: 12px;
$stdMargin: 20px;
@import "../assets/style/common.scss";
footer{
  margin: 50px 0;
  .container-s{
    display: flex;
    .footer_card{
      margin-right: 20px;
      &:last-child{
        margin-right: 0;
      }
      width: 25%;
      font-size: $footerFontSize;
      h2{
        margin-bottom: $stdMargin;
      }
      p{
        color: $blue900;
      }
      a.link{
        color: $blue400;
      }
      img{
        width: 33%;
      }
      .comments{
        margin-top: $stdMargin;
        color: $grey700;
        .fab{
          font-size: 20px;
          margin-right: 15px;
        }
      }
    }
  }
}
</style>
