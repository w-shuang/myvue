<template>
    <div class="icons">
        <swiper>
             <swiper-slide v-for="(page,index) of pages" :key="index">
                <div class="icon" v-for="item of page" :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgurl">
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
             </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: 'HomeIcons',
    data (){
        return {
            iconList: [{
                id: '0001',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
                desc: '经典门票'
            },{
                id: '0002',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc: '一日游'
            },{
                id: '0003',
                imgurl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/5ea666792b98f34c86faea912b5fbcf9.png',
                desc: '玩转周边'
            },{
                id: '0004',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
                desc: '华清宫'
            },{
                id: '0005',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
                desc: '长恨歌'
            },{
                id: '0006',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc: '动植物园'
            },{
                id: '0007',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc: '泡温泉'
            },{
                id: '0008',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc: '兵马俑'
            },{
                id: '0009',
                imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
                desc: '华山'
            }
            ]
        }
    },
    computed: {
        pages (){
            const pages = []
            this.iconList.forEach((item, index) => {
                const page = Math.floor(index / 8)
                if(!pages[page]){
                    pages[page] = []
                }
                pages[page].push(item)
            })
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/varibles.styl'
    @import '~styles/mixins.styl'
    .icons >>> .swiper-container 
        height: 0
        padding-bottom: 50%
    .icons
        margin-top:5px
        .icon  
            position:relative
            overflow: hidden 
            float: left
            width: 25%
            heught: 0 
            padding-bottom: 25%
            .icon-img
                position: absolute
                top: 0
                left: 0
                right: 0
                bottom: 22px
                box-sizing: border-box
                padding: 5px
                .icon-img-content
                    display: block
                    margin: 0 auto
                    height: 100%
            .icon-desc
                position: absolute
                left: 0
                right: 0
                bottom: 0
                height: 22px
                line-height: 22px
                text-align: center
                color: $darkTextColor
                ellipsis()
</style>