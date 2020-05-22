<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <img class="item-img" :src='item.imgurl'>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    data (){
        return {
            recommendList: [{
                id: '0001',
                imgurl: 'http://img1.qunarzz.com/sight/p0/1809/17/171a4af55c089c25a3.img.jpg_200x200_85e86931.jpg',
                title: '太奥幻太奇海洋馆',
                desc:'西二环丰禾路.太奥海洋广场'
            },{
                id: '0002',
                imgurl: 'http://img1.qunarzz.com/sight/p0/1809/17/171a4af55c089c25a3.img.jpg_200x200_85e86931.jpg',
                title: '太奥幻太奇海洋馆',
                desc:'西二环丰禾路.太奥海洋广场'
            },{
                id: '0003',
                imgurl: 'http://img1.qunarzz.com/sight/p0/1809/17/171a4af55c089c25a3.img.jpg_200x200_85e86931.jpg',
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
    .item   
        display: flex
        height: 94px
        overflow: hidden
        .item-img
            width: 85px
            height: 85px
            padding: 5px
        .item-info
            flex:1
            padding: 5px
            min-width:0 
            .item-title
                line-height:27px
                font-size: 16px
                ellipsis()
            .item-desc
                line-height: 20px
                color: #ccc
                ellipsis()
            .item-button
                line-height: 22px
                background: #ff9300
                padding: 0 10px
                border-radius: 3px
                margin-top: 8px
                color: #fff
                border:0


</style>