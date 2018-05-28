<template>
  <div class="message-container">
    <section class="seal-box">
      <img class="seal-img" src="./image/yinzhang.png">
      <span class="seal-title">信息动态</span>
    </section>

    <section class="message-change">
      <div class="message-change-title">
        消息动态
      </div>
      <article class="change1">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="change1">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="change1">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="change1">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="change1">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
    </section>

    <section class="academic-research">
      <div class="academic-research-title">
        联系我们
      </div>
      <article class="connect2">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="connect2">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="connect2">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="connect2">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
      <article class="connect2">
        <span>消息111111111111111111111111111111111111111111111111</span>
        <span>2018-05-12</span>
      </article>
    </section>

    <div class="hr"></div>

    <foots></foots>
  </div>

</template>

<script type="text/ecmascript-6">
  import Foots from '@/components/Front/Frontcomponents/foot'

  export default{
    data() {
      return {
        datas: [],
        id: ''
      }
    },
    methods: {},
    created() {

    },
    components: {
      Foots
    }

  }
</script>

<style lang="stylus" type="text/stylus" rel="stylesheet/stylus">
  .message-container
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
        width :350px
        line-height :27px
        font-size :26px
        color: #5a3224
        font-family: LiSu
    .message-change
      height: 240px
      width: 992px
      margin: 54px auto
      background-image: url(./image/biankuang5.png)
      background-repeat: no-repeat
      background-size: 992px 240px
      overflow: hidden
      color: #5a3224
      font-family:LiSu
      .message-change-title
        margin-top: 20px
        margin-left: 20px
        font-size: 21px
      .change1
        margin-top: 15px
        margin-left: 35px
        margin-right: 45px
        font-size: 19px
        display: flex
        justify-content: space-between
    .academic-research
      height: 240px
      width: 992px
      margin: 54px auto
      background-image: url(./image/biankuang5.png)
      background-repeat: no-repeat
      background-size: 992px 240px
      overflow: hidden
      color: #5a3224
      font-family:LiSu
      .academic-research-title
        margin-top: 20px
        margin-left: 20px
        font-size: 21px
      .connect2
        margin-top: 15px
        margin-left: 35px
        margin-right: 45px
        font-size: 19px
        display: flex
        justify-content: space-between
    .hr
      width: 1200px
      height: 15px
      margin: 38px auto
      background-image: url(./image/fenge2.png)
      background-size: 1200px 15px

</style>
