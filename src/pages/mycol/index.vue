<template>
<div>
<i-grid i-class="no-border">
      <i-grid-item @click="goType(item)" i-class="no-border" v-for="item in grids" :key="item">
          <i-grid-label>{{item.type}}</i-grid-label>
      </i-grid-item>
  </i-grid>
  <i-panel title="我的收藏">
    <view>
      <i-card i-class="split" v-for="item in top" :key="item" :extra="item.type" :thumb="item.img">
          <view slot="content">{{item.content}}</view>
          <view slot="footer">{{item.time}}</view>
      </i-card>
    </view>
  </i-panel>
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
      grids: [
        {type:'图片'},
        {type:'链接'},
        {type:'音乐'},
        {type:'笔记'},
        {type:'位置'}
      ],
      top:[
        {type:"图片",content:"一张图片",time:"10天前"},
        {type:"链接",content:"一个链接",time:"10天前"},
        {type:"音乐",content:"一首音乐",time:"10天前"},
        {type:"笔记",content:"一本笔记",time:"10天前"},
        {type:"位置",content:"一个位置",time:"10天前"},
      ],
    
    }
  },

  components: {
    card
  },
   
  methods: {
    // goList (url) {
    //   mpvue.navigateTo({ url })
    // },
    goType (type) {
      let url = '../collect/main?type=' + type.type
      mpvue.navigateTo({ url })
    }
  },
  created () {
    
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
</style>
