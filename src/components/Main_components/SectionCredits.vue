<template>
    <div class="container-l">
        <img class="bgr_img" src="../../assets/img/brooke-cagle-224821-unsplash-1-1920x700.jpg" alt="Tim Sab">
        <div class="comic">
            <h2>Come as you are</h2>
            <p>MasterStudy used is an exellent workshop whether you come as a counselor, advisor, administrator, or faculty member. I am going home empowered. I am looking forward to attending the On Course MasterStudy and the MasterStudy National Conference next year and facilitating the use of this excellent retention/students succes course at my college.</p>
            <h3>Tim Sab</h3>
            <h4>General Developer, Stylemix Themes</h4>
        </div>
    </div>
</template>

<script>
export default {
  name: "SectionCredits",
  data() {
    return {};
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common.scss";
  .container-l{
    position: relative;
    .bgr_img{
        width: 100%;
    }
    .comic{
        $this-font: 16px;
        color: $blue900;
        h2{
            font-size: calc($this-font * 2.7);
        }
        h2{
            font-weight: 400;
        }
        h3,h4{
            font-weight: 500;
        }
        p{
            padding: 25px 0;
        }
        height: 450px;
        width: 600px;
        background-color: $white;
        padding: 70px;
        position: absolute;
        top: 50%;
        left: 40%;
        transform: translate(-52%, -50%);
        &::after{
            $len: 20px;
            $hei: 20px;
            content: "";
            display: inline-block;
            position: absolute;
            right: -$hei + 1;
            top: calc(50% - ($len / 2));
            width: 0;
            height: 0;
            border-style: solid;
            border-width: $len 0 $len $hei;
            border-color: transparent transparent transparent $white;
        }
    }
  }
</style>