<template>
  <div class="wrapper">
    <swiper :options="swiperOpations" v-if="showSwiper">
      <swiper-slide v-for="item in list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOpations: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true,
        autoplay: 1000,
        paginationClickable: true,
        observeParents: true,
        observer: true
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: white
  .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
      width: 100%
</style>
