<template>
    <div class="header">
       <div class="header-left">返回</div>
       <div class="header-input">输入城市/景点/游玩主题</div>
       <div class="header-right">城市</div>
    </div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
    .header
        display: flex
        line-height: 43px
        height: 43px
        background: #00bcd4
        color: #fff
        .header-left
            width: 32px
            float: left
            margin-right:10px
        .header-input
            flex: 1
            height: 31px
            margin-left: 1px
            background: #fff
            border-radius: 5px
            margin-top: 6px
            color:#ccc
            line-height: 31px
        .header-right
            width: 62px
            float: right
            text-align: center;
</style>
