<template>
  <div id="miaodian0">
    <swiper>
    <swiper-item class="detail-swiper" v-for="(item, index) in topImages" :key="index">
      <img :src="item" alt="">
    </swiper-item>
  </swiper>
  </div>
</template>
<script>
import {Swiper, SwiperItem} from "components/common/swiper/index"

export default {
  name: 'DetailSwiper',
  props: {
    topImages: {
      type: Array,
      default() {
        return []
      }
    }
  },
  components: { 
    Swiper, SwiperItem
  }
}
</script>

<style scoped>
  .detail-swiper {
    height: 300px;
    overflow: hidden;
  }
</style>