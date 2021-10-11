<template>
  <nav ref="navbar">
    <div class="container-l">
        <div class="language">English</div>
        <div class="links">
            <ul class="bar">
                <li class="link" :class="{'new' : element.isNew}" v-for="(element, index) in this.linkArray" :key="index"><a href="#">{{element.name}}</a></li>
            </ul>
            <ul class="bar">
                <li class="social" v-for="(element, index) in this.socialArray" :key="index"><a href="#"><i :class="`fab ${element}`"></i></a></li>
            </ul>
        </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Nav",
  data() {
    return {
        linkArray:[
            {name:"Course",
            isNew:false},
            {name:"Zoom",
            isNew:true},
            {name:"Pages",
            isNew:false},
            {name:"Bundles",
            isNew:false},
            {name:"Courses Formats",
            isNew:false},
            {name:"Add Course",
            isNew:true},
            {name:"Demos",
            isNew:false}
        ],
        socialArray:[`fa-twitter`,`fa-instagram`,`fa-behance`,`fa-dribbble`,`fa-flickr`,`fa-git`,`fa-linkedin`,`fa-pinterest`],
    };
  },
  props:{
      navbarHeight:String,
  },
  methods: {

  },
  mounted(){
    this.$refs.navbar.style.height=this.navbarHeight;
  }
};
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
    nav{
        font-size: 14px;
        border-bottom: 1px solid $grey700;
        .container-l>*{
            color: $grey900!important;
            width: 50%;
        }
        .language{
            &::after{
                margin-left: 14px;
                content: "\f078";
                font-family: "Font Awesome 5 Free";
                font-weight: 600;
                display: inline-block;
            }
        }
        .links{
            display: flex;
            justify-content: space-between;
            .bar{
                display: flex;
                .new::after{
                    position: absolute;
                    font-size: 10px;
                    background-color: $magenta;
                    padding: 2px 5px;
                    top: -14px;
                    right: -10px;
                    display: inline-block;
                    content: "new!";
                    color: white;
                    border-radius: 3px;
                }
                .link{
                    margin-right: 16px;
                    position: relative;
                }
                .social{
                    margin-right: 10px;
                }
            }
        }
    }
</style>
