<template>
  <div class="wrapper">
    <swiper :options="swiperOptions">
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgurl">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default{
    name: 'HomeSwiper',
    data (){
        return {
            swiperOptions: {
                pagination: '.swiper-pagination',
                loop: true
            },
            swiperList: [{
                id: '0001',
                imgurl:'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg'
            },{
                id: '0002',
                imgurl:'http://img1.qunarzz.com/sight/source/1507/fe/679926851c309a.jpg_r_640x214_114816de.jpg'
                }]
        }
    }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background: #fffa
    .wrapper
        width:100%
        height: 0
        overflow: hidden
        padding-bottom: 37.22%
        background: #eee
    .swiper-img
        width: 100%
</style>