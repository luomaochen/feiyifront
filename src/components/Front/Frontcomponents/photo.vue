<template>
  <div class="photo-box">
    <div class="photo-detail1" >
      <article class="photo-item" v-for="n in 4">
        <a href="http://www.w3school.com.cn" target="_blank">
          <img src="./image/lunboimg1.jpg">
        </a>
      </article>
    </div>
    <div class="photo-detail2" >
      <article class="photo-item" v-for="n in 4">
        <a href="http://www.w3school.com.cn" target="_blank">
          <img src="./image/lunboimg2.jpg">
        </a>
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
  .photo-box
    margin-top :32px
    height :318px
    .photo-detail1
      height :143px
      display :flex
      .photo-item
        width :235px
        height :143px
        margin-left :26px
        position:relative;
        &:nth-child(1)
          margin-left :0
        img
          position: absolute;
          top:0;
          left: 0;
          width: 100%;
          height: 100%
          z-index :2
    .photo-detail2
      height :143px
      display :flex
      .photo-item
        width :235px
        height :143px
        margin-left :26px
        margin-top :34px
        position :relative
        &:nth-child(1)
          margin-left :0
        img
          position: absolute;
          top:0;
          left: 0;
          width: 100%;
          height: 100%
          z-index :2

</style>
