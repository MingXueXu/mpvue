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
        {type:'图片与视频'},
        {type:'链接'},
        {type:'音乐'},
        {type:'笔记'},
        {type:'位置'}
      ],
      top:[
        {type:"中国电化教育",content:"个性化学习",time:"9天前"}
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
div >>> .top-padding {
  width:200rpx;
  float: left;

}
.userinfo {
position: relative;
width: 700rpx;
height: 200rpx;
color: #666;
display: flex;
flex-direction: column;
align-items: center;
}
 
.userinfo-avatar {
overflow:hidden;
display: block;
width: 120rpx;
height: 120rpx;
margin: 10rpx;
/* margin-top: 50rpx; */
border-radius: 50%;
border: 2px solid #fff;
box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
}
div>>>.col-class{
  padding-right: 0pt;
  float: left;
  
}
div>>>,col-class1{
   float: right;
}
div>>>.swidth{
  width:155px;
  height:35px;
  background-color: #FFFAF0
}
div>>>.Icolor{
  border-color: #dddee1;
  height: 10px;
  border-style:solid;
  border-width: 0.1ch
}
</style>
