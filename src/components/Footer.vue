<template>
  <footer ref="footer">
    <div class="container-s">
      <div class="footer_card">
        <h2 class="margin_std">About</h2>
        <p>
          <a class="link" href="#">Masterstudy</a> is Education WordPress theme
          featured by Learning Management System (LMS) for online education.
        </p>
        <p class="margin_std">
          Developed by <a href="#" class="link">StylemyxThemes</a>
        </p>
        <p class="comments">
          <a href="#"><i class="fab fa-facebook"></i></a
          ><a href="#"><i class="fab fa-twitter"></i></a
          ><a href="#"><i class="fab fa-instagram"></i></a>
        </p>
      </div>
      <div class="footer_card">
        <h2 class="margin_std">Contact</h2>
        <p class="margin_std">USA, California 20, First Avenue, California</p>
        <p>Tel.: +1 212 458 300 32</p>
        <p class="margin_std">Fax.: +1 212 375 24 14</p>
        <p class="comments"><a href="#">info@masterstudy.com</a></p>
      </div>
      <div class="footer_card">
        <h2 class="margin_std">Pages</h2>
        <div class="lists">
          <ul>
            <li><a href="#"> Blog </a></li>
            <li><a href="#"> Home </a></li>
            <li><a href="#"> Shortcodes </a></li>
          </ul>
          <ul>
            <li><a href="#"> Courses </a></li>
            <li><a href="#"> Membership A... </a></li>
            <li><a href="#"> Typography </a></li>
          </ul>
        </div>
      </div>
      <div class="footer_card">
        <h2 class="margin_std">Blog</h2>
        <div class="blog_miniature">
          <img
            src="../assets/img/photo-1517520287167-4bbf64a00d66-75x75.jpeg"
            alt=""
          />
          <div>
            <h4 class="title">
              Our main target is to "Developing Yourself as a Leader"
            </h4>
            <p class="date">August 9,2018</p>
          </div>
        </div>
        <div class="blog_miniature">
          <img
            src="../assets/img/photo-1490376840453-5f616fbebe5b-50x50.jpeg"
            alt=""
          />
          <div>
            <h4 class="title">
              Those Other College Expenses You Aren' t Thinking About
            </h4>
            <p class="date">June 3,2015</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {},
};
</script>

<style lang="scss" scoped>
$footerFontSize: 12px;
$stdMargin: 20px;
@import "../assets/style/common.scss";
footer {
  margin: 50px 0;
  .margin_std {
    margin-bottom: $stdMargin;
  }
  .container-s {
    display: flex;
    .footer_card {
      .blog_miniature {
        $imgHeight: 60px;
        height: $imgHeight;
        display: flex;
        margin-bottom: calc($stdMargin / 2);
        img {
          height: 100%;
          width: $imgHeight;
          margin-right: 20px;
        }
        h4 {
          color: $grey700;
        }
        .date {
          color: $grey400;
          // margin-left: 2px;
          &:before {
            content: "";
            width: 15px;
            transform: translate(0, -5px);
            display: inline-block;
            border-bottom: 1px solid $grey400;
          }
        }
      }
      .lists {
        display: flex;
        ul {
          list-style: disc;
          width: 50%;
          li {
            margin-bottom: calc($stdMargin / 2);
            color: $blue900;
          }
        }
      }
      margin-right: 20px;
      &:last-child {
        margin-right: 0;
      }
      width: 25%;
      font-size: $footerFontSize;
      p {
        color: $blue900;
      }
      a.link {
        color: $blue400;
      }
      img {
        width: 33%;
      }
      .comments {
        color: $grey700;
        .fab {
          font-size: 20px;
          margin-right: 15px;
        }
      }
    }
  }
}
</style>
