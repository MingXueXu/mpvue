<template>
<div>
 <i-input type="text" placeholder="搜索" i-class ="Icolor"/>
 <i-grid i-class="no-border">
      <i-grid-item @click="goList(item.url)" i-class="no-border" v-for="item in grids" :key="item">
          <i-grid-label>{{item.type}}</i-grid-label>
      </i-grid-item>
  </i-grid>
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
        {type:'图片与视频'},
        {type:'链接'},
        {type:'文件'},
        {type:'音乐'},
        {type:'笔记'}
      ],
      recommand: top
  }
  },
  methods:{
       goList (url) {
      mpvue.navigateTo({ url })
    },
    goType (type) {
      let url = '../list/main?type=' + type
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
div >>> .split {
  margin-bottom: 10pt;
}
</style>
