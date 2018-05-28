<template>
  <div class="feiyideatil-container">
    <header class="other-header">
      <div class="header-left">
        <img class="logo-img" src="./image/LOGO.png">
        <div class="logo-title">
          中国体育
        </div>
        <div class="logo-title">
          非物质文化遗产
        </div>
      </div>
      <div class="header-right">
        <article class="nav-article">
          <form class="art-form">
            <input class="art-input" type="text" name="username"/>
            <div class="art-submit"><a href="#">搜索</a></div>
          </form>
        </article>
        <nav class="nav">
          <ul class="nav-ul">
            <li @click="go('Home_index')">首页</li>
            <li><router-link class="other-href other-href3" :class="qq ? 'other-href1' : 'other-href2' " to="/other/feiyi">非遗项目</router-link></li>
            <!--<li><router-link class="other-href" to="/other/next">传承人</router-link></li>-->
            <li><router-link class="other-href" to="/other/message">信息动态</router-link></li>
            <!--<li><router-link class="other-href" to="/other/abroad">域外项目</router-link></li>-->
            <li><router-link class="other-href" to="/other/myself">关于我们</router-link></li>
          </ul>
        </nav>
      </div>
    </header>
    <div class="hr"></div>


    <section class="nav-top">
      <section class="seal-box" >
        <img class="seal-img"  src="./image/yinzhang.png">
        <span class="seal-title">XXXXX项目</span>
      </section>
      <section class="detail-info">
        <span >项目编号：A11111111</span>
        <span >项目地区：新疆</span>
      </section>
    </section>

    <section class="detail-all" v-for="n in 7">
      <div class="detail-all-title">
        概述
      </div>
      <div class="detail-all-messagebox">
        <p class="detail-all-content">
          据推测，夏至应该是其中之一。古代中国最初使用“土圭日影法”来测定一年中白昼最长和最短的日子，
          《周礼·地官》中的“大司徒”一则说：“以土圭之法，测土深，正日景，以求地中。”可见，先人采用
          土圭测日影的方法，发现这一天白昼最长，夜晚最短，因而确定了夏至，后来又发展为二十四节气之一。
        </p>
        <img class="detail-all-img" src="./image/lunboimg2.jpg">
      </div>
    </section>

    <section class="detail-map">
      <div class="detail-map-title">
        项目地图
      </div>
      <div class="detail-map-box">
        <maps></maps>
      </div>
    </section>


    <section class="relevant-img">
      <div class="relevant-img-title">
        相关图片
      </div>
      <div class="flex-box">
      <div class="relevant-img-box" v-for="n in 4">
        <img  src="./image/lunboimg2.jpg">
        <div class="relevant-img-content">
          图片描述XXXXX
        </div>
      </div>
      </div>
    </section>

    <section class="relevant-video">
      <div class="relevant-video-title">
        相关视频
      </div>
      <div class="flex-box">
        <div class="relevant-video-box" v-for="n in 4">
          <video src="./image/movie.mp4">
            您的浏览器不支持video
          </video>
          <div class="relevant-video-content">
            视频描述XXXXX
          </div>
        </div>
      </div>
    </section>

    <section class="connect-us">
      <div class="connect-us-title">
        项目动态
      </div>
      <article class="connect1">
        项目动态 1111111111111111111111111111111111111111
      </article>
      <article class="connect1">
        项目动态 1111111111111111111111111111111111111111
      </article>
      <article class="connect1">
        项目动态 1111111111111111111111111111111111111111
      </article>
      <article class="connect1">
        项目动态 1111111111111111111111111111111111111111
      </article>
      <article class="connect1">
        项目动态 1111111111111111111111111111111111111111
      </article>
    </section>

    <div class="hr"></div>
    <foots></foots>
  </div>

</template>

<script type="text/ecmascript-6">
  import Maps from '@/components/Front/Frontcomponents/map'
  import Foots from '@/components/Front/Frontcomponents/foot'

  export default{
    data() {
      return {
        datas: [],
        id: ''
      }
    },
    methods: {
      go(name){
        this.$router.push({
          name: name
        })
      }
    },
    created() {

    },
    components: {
        Maps,
        Foots
    }

  }
</script>

<style lang="stylus" type="text/stylus" rel="stylesheet/stylus">


  .other-href3
    color red
    background-image: url(./image/huizhang.png)
    background-repeat: no-repeat
    background-size: 100% 100%


.feiyideatil-container
  width :1200px
  height:100%
  margin :auto
  .other-header
    height :180px
    width :100%
    display :flex
    .header-left
      display :block
      width :130px
      height :105px
      margin-left :80px
      margin-top :63px
      .logo-img
        width :96px
        height :60px
        display :block
        margin :auto
      .logo-title
        width :130px
        color: #5a3223
        font-size: 16px
        font-family:LiSu
        text-align :center
    .header-right
      margin-left:30px
      width :958px
      .nav-article
        margin-top: 52px
        width :350px
        height :38px
        float: right
        margin-right :78px
        .art-form
          margin: auto
          width: 350px
          height: 38px
          display: flex
          .art-input
            width: 270px
            height: 34px
            border-radius: 10px
            font-size: 23px
            font-family:LiSu
            outline: none
          .art-submit
            background-color: #d4c7ad
            line-height: 38px
            text-align: center
            margin-left: 30px
            font-size: 23px
            font-family:LiSu
            height: 38px
            width: 50px
            border-radius: 10px
            a
              text-decoration: none
              color: #5a3224
      .nav
        clear both
        width: 841px
        height: 38px
        margin-top :118px
        margin-left :50px
        .nav-ul
          list-style: none
          li
            float: left
            line-height: 38px
            text-align: center
            margin-left: 50px
            font-size: 30px
            text-decoration: none
            color: #5a3224
            font-family:LiSu
            cursor: pointer
            a
              text-decoration: none
              color: #5a3224
  .hr
    width: 1200px
    height: 15px
    margin: 0 auto
    background-image: url(./image/fenge2.png)
    background-size: 1200px 15px


  .nav-top
    display :flex
    justify-content:space-between
    width :1200px
    height :132px
    margin :10px auto
    margin-bottom :0
    .seal-box
      margin-top :25px
      display :flex
      margin-left :132px
      margin-bottom :10px
      .seal-img
        width :16px
        height :27px
      .seal-title
        height :27px
        width :350px
        line-height :27px
        font-size :26px
        color: #5a3224
        font-family: LiSu
    .detail-info
      width :50%
      height :100%
      color: #5a3223
      font-size: 16px
      font-family:LiSu
      span
        display inline-block
        margin-top :35px
        margin-right :25px
        float right
        &:nth-child(1)
          margin-right :150px


  .detail-all
    width :975px
    height :280px
    margin :80px auto
    background-image: url(./image/biankuang6.png)
    background-repeat: no-repeat
    background-size: 975px 280px
    overflow :hidden
    cursor :pointer
    .detail-all-title
      color: #5a3223
      font-size: 23px
      font-family:LiSu
      margin-top :20px
      margin-left :20px
    .detail-all-messagebox
      height :75%
      width :95%
      margin : auto
      display flex
      .detail-all-content
        width :70%
        height :85%
        margin-left :10px
        margin-top :20px
        color: #5a3223
        font-size: 19px
        font-family:LiSu
      .detail-all-img
        width :300px
        height :180px
        display :inline-block
        margin-top :30px
        margin-left :20px



  .detail-map
    width :990px
    height :480px
    margin :132px auto
    margin-bottom :0
    padding-top :1px
    background-image: url(./image/biankuang2.png)
    background-repeat: no-repeat
    background-size: 990px 480px
    .detail-map-title
      font-size :21px
      color: #5a3224
      font-family:LiSu
      margin-top :15px
      margin-left :20px
    .detail-map-box
      margin :15px 0 0 50px
      width :920px
      height :420px



  .relevant-img
    width :988px
    height :270px
    margin :50px auto
    background-image: url(./image/biankuang6.png)
    background-repeat: no-repeat
    background-size: 988px 270px
    overflow :hidden
    .relevant-img-title
      color: #5a3223
      font-size: 21px
      font-family:LiSu
      margin-top :20px
      margin-left :20px
      margin-bottom :20px
    .flex-box
      display :flex
      .relevant-img-box
        width :220px
        height :190px
        margin-left :23px
        margin-top :20x
        img
          width :220px
          height :160px
        .relevant-img-content
          text-align :center
          color: #5a3223
          font-size: 18px
          font-family:LiSu

  .relevant-video
    width :988px
    height :270px
    margin :50px auto
    background-image: url(./image/biankuang6.png)
    background-repeat: no-repeat
    background-size: 988px 270px
    overflow :hidden
    .relevant-video-title
      color: #5a3223
      font-size: 21px
      font-family:LiSu
      margin-top :20px
      margin-left :20px
      margin-bottom :20px
    .flex-box
      display :flex
      .relevant-video-box
        width :220px
        height :190px
        margin-left :23px
        margin-top :20x
        video
          width :210px
          height :160px
        .relevant-video-content
          text-align :center
          color: #5a3223
          font-size: 18px
          font-family:LiSu

  .connect-us
    height :300px
    width :642px
    margin-left :110px
    margin-bottom :40px
    background-image: url(./image/biankuang6.png)
    background-repeat: no-repeat
    background-size: 642px 300px
    overflow :hidden
    color: #5a3224
    font-family: LiSu
    .connect-us-title
      margin-top :20px
      margin-left :20px
      font-size :21px
    .connect1
      margin-top :25px
      margin-left :35px
      font-size :19px
</style>



