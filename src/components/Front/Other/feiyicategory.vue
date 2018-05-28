<template>
  <div class="other-category-container">
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

    <section class="seal-box">
      <img class="seal-img" src="./image/yinzhang.png">
      <span class="seal-title" style="width:300px">非遗项目>类别</span>
    </section>

    <section class="eachcategory-container">
      <div class="eachcategory-box" @click="go('Detail')" v-for="n in 10">
        <img src="./image/lunboimg2.jpg">
        <div>
          <p class="eachcategory-box-title">项目名称</p>
          <p class="eachcategory-box-content">项目概述: 阿瑟斯发射点发射点士大。夫十分手动阀手动阀，手动阀手动阀手动阀手动阀是？</p>
        </div>
      </div>
    </section>
    <foots></foots>
  </div>
</template>

<script type="text/ecmascript-6">
  import Foots from '@/components/Front/Frontcomponents/foot'

  export default{
    data() {
      return {
        datas: [],
        id: '',
        qq: '',
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





.other-category-container
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
  .seal-box
    margin-top :35px
    display :flex
    margin-left :132px
    margin-bottom :10px
    .seal-img
      width :16px
      height :27px
    .seal-title
      height :27px
      width :150px
      line-height :27px
      font-size :26px
      color: #5a3224
      font-family: LiSu

  .eachcategory-container
    width: 1200px
    margin: 2px auto
    display flex
    flex-wrap:wrap
    flex-direction: row
    .eachcategory-box
      cursor :pointer
      width :480px
      height :150px
      margin-left :50px
      margin-right :50px
      margin-top :80px
      display flex
      background-image: url(./image/biankuang8.png)
      background-repeat: no-repeat
      background-size: 480px 150px
      img
        display block
        width :156px
        height :123px
        margin-top :15px
        margin-left :15px
        ~ div
          width :278px
          height :100px
          margin-left :10px
          margin-top :28px
          color: #5a3224
          font-family:LiSu
          font-weight :400
          .eachcategory-box-title
             font-size :16px
          .eachcategory-box-content
             font-size :14px

</style>
