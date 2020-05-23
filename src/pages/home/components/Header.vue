<template>
    <div class="header">
       <div class="header-left">
         <div class="iconfont back-icon">&#xe624;</div>
       </div>
       <div class="header-input">
         <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
       </div>
       <div class="header-right">{{this.city}}
         <span class="iconfont arrow-icon">&#xe6aa;</span>
       </div>
    </div>
</template>

<script>
export default{
  name: 'HomeHeader',
  props:{
    city: String
  }

}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    .header
        display: flex
        line-height: 43px
        height: 43px
        background: $bgColor
        color: #fff
        .header-left
            width: 32px
            float: left
            margin-right:10px
            .back-icon
                text-align: center
                font-size: 20px
        .header-input
            flex: 1
            height: 31px
            margin-left: 1px
            background: #fff
            border-radius: 5px
            margin-top: 6px
            padding-left: 10px
            color:#ccc
            line-height: 31px
        .header-right
            width: 62px
            float: right
            text-align: center;
            .arrow-icon
                margin-left: -2px
                font-size:12px
</style>
