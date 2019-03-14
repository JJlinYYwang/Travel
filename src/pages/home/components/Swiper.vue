<template>
    <div class="wrapper">
    <swiper :options="swiperOption" >
        <swiper-slide v-for= "item of swiperList" :key = "item.id">
            <img  class = "swiper-img" :src= "item.imageUrl"  >
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
    </div>

</template>

<script>

export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001 ',
        imageUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/ad906cbe02849a504c4a4399741013a4.jpg_750x200_8ac64dcc.jpg'
      },
      {
        id: '0002',
        imageUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20192/9f73976e40c4ef845cabe0efc0269ebb.jpg_750x200_aab92b7a.jpg'
      }]

    }
  }
}
</script>

<style  lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
      background-color :#fff
    .wrapper
        overflow :hidden
        width : 100%
        height : 0
        padding-bottom 32.67%
        .swiper-img
            width:100%
</style>
