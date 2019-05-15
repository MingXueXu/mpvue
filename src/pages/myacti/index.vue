<template>
<div>
  <swiper
      :indicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
      style="height:200px"
    >
    <block v-for="item in imgUrls" :key="item">
      <swiper-item>
        <image :src="item" style="width:100%;"/>
      </swiper-item>
    </block>
  </swiper>
</div>
</template>

<script>

import card from '@/components/card'

export default {
  components: {
    card
  },

  data () {
    return {
      imgUrls: [
        'http://lib.hubu.edu.cn/__local/D/7D/40/5F49483FCAF7618B97E9B7921F4_2AE8D7B9_CC5F6.png',
        'http://lib.hubu.edu.cn/__local/F/9A/8D/119B34B058589951181625A779D_4C8288CD_62F7B.png',
        'http://lib.hubu.edu.cn/__local/0/9A/63/909E397D1EED8910849D4652065_74A49A9C_6AC6D.jpg'
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 5000,
      duration: 1000,
    }
  },
  methods:{
     
  },
  created () {
    
  }
}
</script>

<style scoped>

</style>
