<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src='item.imgurl'>
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeWeekend',
    data (){
        return {
            recommendList: [{
                id: '0001',
                imgurl: 'http://img1.qunarzz.com/sight/source/1505/30/67d5e62ca78a29.jpg_r_640x214_9dfb4295.jpg',
                title: '太奥幻太奇海洋馆',
                desc:'西二环丰禾路.太奥海洋广场'
            },{
                id: '0002',
                imgurl: 'http://img1.qunarzz.com/sight/source/1507/de/e6ba44d61894c0.jpg_r_640x214_847324d0.jpg',
                title: '太奥幻太奇海洋馆',
                desc:'西二环丰禾路.太奥海洋广场'
            },{
                id: '0003',
                imgurl: 'http://img1.qunarzz.com/sight/source/1507/fe/679926851c309a.jpg_r_640x214_114816de.jpg',
                title: '太奥幻太奇海洋馆',
                desc:'西二环丰禾路.太奥海洋广场'
            }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
   @import '~styles/mixins.styl'
    .title
        margin-top: 10px
        line-height:40px
        background: #eee
        text-indent: 10px
    .item-img-wrapper
        height:0
        overflow:hidden
        padding-bottom: 33.9%
        .item-img
            width: 100%
    .item-info
        padding: 5px
    .item-title
        line-height:27px
        font-size: 16px
        ellipsis()
    .item-desc
        line-height: 20px
        color: #ccc
        ellipsis()
</style>