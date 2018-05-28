<template>
  <div class="two-container">
    <div class="hot-container">
      <img class="hot-title" src="./image/title-remen.png">
      <span class="hot-more">更多></span>
      <article class="hot-item">
        <div class="hot-item-title">
          项目1 名称
        </div>
        <div class="hot-item-detail">
          项目1 概述
        </div>
        <div class="hot-item-content">
          阳光，水润一样，从遥远的天际，射出她艳美的光束，以独特的韵致，染绿着天空的蔚蓝
        </div>
      </article>
      <article class="hot-item">
        <div class="hot-item-title">
          项目2 名称
        </div>
        <div class="hot-item-detail">
          项目2 概述
        </div>
        <div class="hot-item-content">
          如水一样的月，在太空盯着我傻笑，妩媚地，如有一丝少女的味道。
        </div>
      </article>
      <article class="hot-item">
        <div class="hot-item-title">
          项目3 名称
        </div>
        <div class="hot-item-detail">
          项目3 概述
        </div>
        <div class="hot-item-content">
          阳光，水润一样，从遥远的天际，射出她艳美的光束，以独特的韵致，染绿着天空的蔚蓝
        </div>
      </article>
      <article class="hot-item">
        <div class="hot-item-title">
          项目4 名称
        </div>
        <div class="hot-item-detail">
          项目4 概述
        </div>
        <div class="hot-item-content">
          哈哈，我不禁傻傻痴笑，那种笑，是苦涩，是香溢，亦或甜蜜。总而言之，
        </div>
      </article>
    </div>
    <div class="wonderful-container">
      <img class="won-title" src="./image/title-jingcai.png">
      <span class="won-more">更多></span>
      <div class="won-img-item">
        <img class="won-img" src="./image/lunboimg1.jpg">
        <article class="won-item1">
          <div class="won-item-title">
            项目1 名称
          </div>
          <div class="won-item-detail">
            项目1 概述
          </div>
          <div class="won-item-content">
            阳光，水润一样，从遥远的天际，射出她艳美的光束
          </div>
        </article>
      </div>
      <article class="won-item" style="margin-top: -10px">
        <div class="won-item-title">
          项目2 名称
        </div>
        <div class="won-item-detail">
          项目2 概述
        </div>
        <div class="won-item-content">
          如水一样的月，在太空盯着我傻笑，妩媚地，如有一丝少女的味道.
        </div>
      </article>
      <article class="won-item">
        <div class="won-item-title">
          项目3 名称
        </div>
        <div class="won-item-detail">
          项目3 概述
        </div>
        <div class="won-item-content">
          如水一样的月，在太空盯着我傻笑，妩媚地，如有一丝少女的味道。
        </div>
      </article>
      <article class="won-item">
        <div class="won-item-title">
          项目4 名称
        </div>
        <div class="won-item-detail">
          项目4 概述
        </div>
        <div class="won-item-content">
          如水一样的月，在太空盯着我傻笑，妩媚地，如有一丝少女的味道。
        </div>
      </article>

    </div>
  </div>

</template>

<script type="text/ecmascript-6">

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
        components: {}

    }
</script>

<style lang="stylus" type="text/stylus" rel="stylesheet/stylus">

  .two-container
    display: flex
    .hot-container
      width: 475px
      height: 540px
      background-image: url(./image/remenjingcai.png)
      background-repeat: no-repeat
      background-size: 475px 540px
      position: relative
      .hot-title
        margin: 34px 0 20px 26px
      .hot-more
        position: absolute
        top: 26px
        left: 395px
        font-size: 12pt
        font-family: LiSu
        color: #5a3224
        width: 80%
      .hot-item
        margin-top: 20px
        margin-left: 32px
        width: 88%
        height: 83px
        font-family:LiSu
        color: #5a3224
        .hot-item-title
          font-size: 14pt
          font-weight: bold
        .hot-item-detail
          margin-top: 8px
          margin-bottom: 5px
          font-size: 13pt
          font-weight: 500
        .hot-item-content
          font-size: 12pt
          font-weight: 500

    .wonderful-container
      margin-left: 104px
      width: 475px
      height: 540px
      background-image: url(./image/remenjingcai.png)
      background-repeat: no-repeat
      background-size: 475px 540px
      position: relative
      .won-title
        margin: 34px 0 20px 26px
      .won-more
        position: absolute
        top: 26px
        left: 395px
        font-size: 12pt
        font-family: LiSu
        color: #5a3224
        width: 80%
      .won-img-item
        height: 102px
        display: flex
        margin-bottom:30px
        .won-img
          height: 90px
          width: 130px
          margin-left: 32px
          border solid #875c2e
        .won-item1
          margin-top: 20px
          margin-left: 32px
          width: 258px
          height: 83px
          font-family:LiSu
          color: #5a3224
          .won-item-title
            font-size: 14pt
            font-weight: bold
          .won-item-detail
            margin-top: 4px
            margin-bottom: 5px
            font-size: 13pt
            font-weight: 500
          .won-item-content
            font-size: 12pt
            font-weight: 500
      .won-item
        margin-top: 20px
        margin-left:32px
        width: 88%
        height: 83px
        font-family:LiSu
        color: #5a3224
        .won-item-title
          font-size: 14pt
          font-weight: bold
        .won-item-detail
          margin-top: 8px
          margin-bottom: 5px
          font-size: 13pt
          font-weight: 500
        .won-item-content
          font-size: 12pt
          font-weight: 500
</style>
