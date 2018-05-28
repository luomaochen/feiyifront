<template>
  <div>
  <div class="index-wrapper">
    <header class="header-container">
        <img class="head-image" src="./image/logo.png">
        <span class="head-title">中国体育非物质文化遗产</span>
        <p class="head-info">各族人民世代相承与群众生活密切相关各种传统文化表现形式和文化空间</p>
    </header>
    <nav class="nav-container">
      <ul class="nav-ul">
        <li >首页</li>
        <li @click="go('Other')">非遗项目</li>
        <!--<li @click="go('Next')">传承人</li>-->
        <li @click="go('Message')">信息动态</li>
        <!--<li @click="go('Abroad')">域外项目</li>-->
        <li @click="go('Myself')">关于我们</li>
      </ul>
    </nav>
    <section class="search-container">
      <form class="search-form">
        <input class="search-input" type="text" name="username"/>
        <div class="search-submit"><a href="#">搜索</a></div>
      </form>
    </section>
    <section class="lunbo-container">
      <div id="lunbo-box">
        <div class="title-left">
          <span>图片标题</span>
          <p>这是一幅非常不错的不错的体育运动图片这真的很棒！是一幅非常不错的不错的体育运动图片这真的很棒</p>
        </div>
        <div class="swiper">
          <swiper :options="swiperOption" ref="mySwiper">
            <swiper-slide class="swiper-slide games"><img src="./image/lunboimg1.jpg"></swiper-slide>
            <swiper-slide class="swiper-slide games"><img src="./image/lunboimg2.jpg"></swiper-slide>
            <swiper-slide class="swiper-slide games"><img src="./image/lunboimg3.jpg"></swiper-slide>
            <swiper-slide class="swiper-slide games"><img src="./image/lunboimg4.jpg"></swiper-slide>
            <swiper-slide class="swiper-slide games"><img src="./image/lunboimg5.jpg"></swiper-slide>
          </swiper>
        </div>
        <div class="title-right">
          <img src="./image/yinzhang.png">
          <div class="swiper-pagination"></div>
        </div>
      </div>
    </section>
    <div class="hr"></div>
    <section class="retrieval-container">
      <myhr hrimg="/static/kuaisujs.png"></myhr>
      <article class="retrieval-category">
        <span>
          <div><img src="./image/wushu.png"></div>
          <div class="category-title">武术类</div>
        </span>
        <span>
          <div><img src="./image/qiu.png"></div>
          <div class="category-title">球类</div>
        </span>
        <span>
          <div><img src="./image/shuaijiao.png"></div>
          <div class="category-title">摔跤类</div>
        </span>
        <span>
          <div><img src="./image/jingdu.png"></div>
          <div class="category-title">竞渡类</div>
        </span>
        <span>
          <div><img src="./image/youxi.png"></div>
          <div class="category-title">游戏类</div>
        </span>
        <span>
          <div><img src="./image/wulong.png"></div>
          <div class="category-title">舞龙类</div>
        </span>
        <span>
          <div><img src="./image/wushi.png"></div>
          <div class="category-title">舞狮类</div>
        </span>
        <span>
          <div><img src="./image/jianwu.png"></div>
          <div class="category-title">健舞类</div>
        </span>
        <span>
          <div><img src="./image/saihui.png"></div>
          <div class="category-title">赛会类</div>
        </span>
      </article>
      <article class="level">
        <span>国家级</span>
        <span>省级</span>
        <span>市级</span>
        <span>县级</span>
      </article>
    </section>
    <section class="Map-container">
      <myhr hrimg="/static/xiangmuditu.png"></myhr>
      <div class="Map-box">
        <maps class="maps"></maps>
      </div>
    </section>
    <div class="hr"></div>
    <section class="hot">
      <hots></hots>
    </section>
    <div class="hr"></div>
    <section class="video">
      <myhr hrimg="/static/xiangmuvideo.png"></myhr>
      <videos></videos>
    </section>
    <section class="photo">
      <myhr hrimg="/static/xiangmuphoto.png"></myhr>
      <photos></photos>
    </section>

    <section class="href">
      <span class="href-title">友情连接：</span>
      <span class="href-content"><a href="#">XXXXXXXXXXXX</a></span>
      <span class="href-content"><a href="#">XXXXXXXXXXXX</a></span>
      <span class="href-content"><a href="#">XXXXXXXXXXXX</a></span>
      <span class="href-content"><a href="#">XXXXXXXXXXXX</a></span>
    </section>
    <div class="hr"></div>
    <foots></foots>


  </div>
  <div class="index2-wrapper">
    <div class="index2-box">
      <img class="bk-imge1" src="./image/bkimg1.png">
      <img class="bk-img2" src="./image/bkimg2.png">

      <img class="bk-img3" src="./image/bkimg3.png">
      <img class="bk-img4" src="./image/bkimg4.png">
      <img class="bk-img5" src="./image/bkimg5.png">
    </div>

  </div>
  </div>
</template>

<script type="text/ecmascript-6">
  import 'swiper/dist/css/swiper.css'
  import {swiper, swiperSlide} from 'vue-awesome-swiper'
  import Myhr from '@/components/Front/Frontcomponents/hr'
  import Maps from '@/components/Front/Frontcomponents/map'
  import Hots from '@/components/Front/Frontcomponents/hot'
  import Photos from '@/components/Front/Frontcomponents/photo'
  import Videos from '@/components/Front/Frontcomponents/video'
  import Foots from '@/components/Front/Frontcomponents/foot'

  export default {
    name: 'carrousel',
    data () {
      return {
        swiperOption: {
          // swiper configs 所有的配置同swiper官方api配置
          autoplay: {
            delay: 3000,//5秒切换一次
          },
          effect: 'fade',
          pagination: {
            el: '.swiper-pagination',
            clickable: true,
            renderBullet: function (index, className) {
              return '<span class="' + className + '" style="color:#5a3223">' + (index + 1) + '</span>';
            },
          },
          loop: true,
        }
      }
    },
    methods: {
      go(name){
        this.$router.push({
          name: name
        })
      }
    },
    components: {
      swiper,
      swiperSlide,
      Myhr,
      Maps,
      Photos,
      Videos,
      Hots,
      Foots
    },
    mounted() {

    }
  }
</script>

<style lang="stylus" type="text/stylus" rel="stylesheet/stylus">
.index-wrapper
// background-image:url(./image/background1.jpg)
  z-index :-10
  width :1200px
  height :100%
  margin auto
  overflow hidden
  .header-container
    height: 88px
    width: 785px
    margin-left :80px
    margin-top :55px
    color: #5a3223
    font-family: LiSu
    .head-image
      margin-top: 4px
      height: 35px
      width: 52px
    .head-title
      margin-left: 5px
      font-size: 47pt
      font-weight: 500
    .head-info
      margin-top: 6px
      font-size: 15pt
      font-weight: 500

  .nav-container
    width: 1096px
    height: 40px
    margin: 12px auto
    background-image: url(./image/fenge1.png)
    background-size: 1096px 40px
    .nav-ul
      list-style: none
      li
        float: left
        line-height: 35px
        text-align: center
        margin-left: 80px
        font-size: 32pt
        text-decoration: none
        color: #5a3224
        font-family:LiSu
        cursor: pointer

  .search-container
    margin: 11px
    .search-form
      margin: auto
      width: 641px
      height: 36px
      display: flex
      .search-input
        width: 508px
        height: 36px
        border-radius: 10px
        font-size: 32px
        font-family:LiSu
        outline: none
      .search-submit
        background-color: #5a3223
        line-height: 40px
        text-align: center
        margin-left: 15px
        font-size: 32pt
        font-family:LiSu
        height: 40px
        width: 118px
        border-radius: 10px
        a
          text-decoration: none
          color :#FEFEFE

  .lunbo-container
    width: 90%
    height: 365px
    margin: auto
    position: relative
    background-image: url(./image/juanzhou.png)
    background-repeat: no-repeat
    z-index :1
    background-size: 100% 365px
    #lunbo-box
      position: absolute
      top: 30px
      left: 6.5%
      margin: auto
      width: 87%
      height: 306px
      display: flex
      .title-left
        width: 142px
        height :300px
        writing-mode: vertical-lr /*从左向右 从右向左是 writing-mode: vertical-rl;*/
        margin-top: 4px
        margin-left :15px
        font-family:LiSu
        font-size: 25px
        color: #5a3224
        span
          width :24px
          height :80px
          font-size :14pt
          display :block
          margin-left :20px
          font-weight :600
        p
          width :38px
          height :298px
          font-size :12pt
          margin-left :0
          line-height :22px
          font-weight :500

      .swiper
        width: 600px
        height: 300px
        margin-left :20px
        margin-right :20px
        margin-top :4px
        .swiper-slide
          width: 600px
          height: 300px
          img
            width: 600px
            height: 300px
      .title-right
        width: 142px
        height :300px
        margin-top: 4px
        margin-right :18px
        img
          display block
          margin:36px auto
          width: 36px
          height: 36px
        .swiper-pagination
          position: relative
          width: 30px
          margin:36px auto
        .swiper-pagination-bullet
          width: 23px
          height: 23px
          line-height: 23px
          color: #5a3223
          text-align: center
          margin-top: 8px
          border: solid #9a7c69
          background: rgb(255, 255, 255)
        .swiper-pagination-bullet-active
          background: #898989

  .hr
    width: 1100px
    height: 10px
    margin: 19px auto
    background-image: url(./image/fenge2.png)
    background-size: 1100px 10px

  .retrieval-container
    width: 1064px
    height: 215px
    margin: auto
    .retrieval-category
      margin-top: 15px
      display: flex
      span
        width: 100px
        height: 110px
        margin-left: 17px
        img
          display: block
          width: 100px
          height: 70px
          margin: auto
          text-align: center
        .category-title
          width: 100px
          height: 40px
          margin: auto
          text-align: center
          font-size: 25pt
          color: #5a3324
          font-family:LiSu
    .level
      margin-top: 5px
      span
        width: 100px
        height: 40px
        margin-left: 18px
        text-align: center
        font-size: 35px
        color: #5a3324
        font-family:LiSu

  .Map-container
    height: 520px
    width: 1000px
    margin: 10px auto
    z-index :2
    .Map-box
      width: 960px
      height: 450px
      margin: 30px auto
      background-image: url(./image/Mapbiankuang.png)
      background-repeat: no-repeat
      background-size: 960px 450px
      display: flex
      z-index :2
      .maps
        margin: auto
        z-index :2


  .hot
    height: 540px
    width 1054px
    margin: 56px auto
  .video
    height: 400px
    width: 1022px
    margin: 25px auto
    z-index :2
  .photo
    height: 400px
    width: 1022px
    margin: 25px auto


  .href
    height :18px
    width :600px
    margin-left:105px
    margin-top :48px
    color: #5a3224
    font-family:LiSu
    .href-title
      font-size: 14pt
    .href-content
      a
        color: #5a3224
        font-size: 14pt
        text-decoration: none




.index2-wrapper
  z-index:-2
  position absolute
  top :0
  left :0
  height :3000px
  width :100%
  .index2-box
    z-index :-2
    position relative
    margin auto
    height :100%
    width :1400px
    .bk-imge1
      position :absolute
      z-index :0
      width :550px
      height :320px
      top :720px
      right:2px
    .bk-img2
      position :absolute
      z-index :0
      width :370px
      height :530px
      top :2060px
      left :0
    .bk-img3
      position :absolute
      z-index :0
      width :480px
      height :260px
      top :1390px
      left :0
    .bk-img4
      position :absolute
      z-index :0
      width :390px
      height :409px
      top :2000px
      right :0
    .bk-img5
      position :absolute
      z-index :0
      width :325px
      height :345px
      top :2750px
      right :0

</style>
