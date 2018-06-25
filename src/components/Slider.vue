<template>
    <Carousel :perPageCustom='[[768, 1], [1024, 3]]' :perPage='1' class='mt-5 pt-5'>
        <Slide v-for='(slide, index) in slides' :key='index'>
                <router-link :to='slide.link'>
                    <img :src='slide.src' alt=''>
                </router-link>
        </Slide>
    </Carousel>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'

export default {
  data () {
    return {
      slides: [
        {src: require('../assets/img/1.jpg'), link: '/about'},
        {src: require('../assets/img/2.jpg'), link: '/contact'},
        {src: require('../assets/img/3.jpg'), link: '/'},
        {src: require('../assets/img/4.jpg'), link: '/contact'}
      ]
    }
  },
  name: 'Slider',
  components: {
    Carousel,
    Slide
  }
}
</script>

<style lang='stylus' scoped>
  .VueCarousel-inner 
    > div 
      padding 0
      margin 0
      list-style none
      display flex
      align-items center
      justify-content center
</style>