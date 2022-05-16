<template>
  <swiper>
      <swiper-item v-for="(item,index) in banners" :key="index">      
        <a :href="item.link">
          <img :src="item.image">
        </a>
      </swiper-item>
    </swiper>
</template>

<script>
import {Swiper,SwiperItem} from 'components/common/swiper'
// import Swiper from 'components/common/swiper/Swiper'
// import SwiperItem from 'components/common/swiper/SwiperItem'
export default {
    name:'homeswiper',
    props: {
        banners:{
            type:Array,
            default(){
                return []
            }
        }
    },
    components: {
      Swiper,
      SwiperItem
    }
}
</script>

<style scoped>
    img{width: 100%;}
</style>