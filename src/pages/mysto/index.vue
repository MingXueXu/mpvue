<template>
<div>
  <i-divider content="喜欢的书都可以放在这里哦" color="#2d8cf0" lineColor="#2d8cf0"></i-divider>
 <i-panel title="我的书架">
     <i-row>
    <i-col span="8" i-class="col-class">  <view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">明朝那些事</view>
        <view slot="footer">评分：9.5</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">追风筝的人</view>
        <view slot="footer">评分：9.1</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">我们仨</view>
        <view slot="footer">评分：9.0</view>
      </i-card></i-col>
</i-row>
<i-row>
    <i-col span="8" i-class="col-class">  <view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">明朝那些事</view>
        <view slot="footer">评分：9.5</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">追风筝的人</view>
        <view slot="footer">评分：9.1</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">我们仨</view>
        <view slot="footer">评分：9.0</view>
      </i-card></i-col>
</i-row>
<i-row>
    <i-col span="8" i-class="col-class">  <view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">明朝那些事</view>
        <view slot="footer">评分：9.5</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">追风筝的人</view>
        <view slot="footer">评分：9.1</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">我们仨</view>
        <view slot="footer">评分：9.0</view>
      </i-card></i-col>
</i-row>
<i-row>
    <i-col span="8" i-class="col-class">  <view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">明朝那些事</view>
        <view slot="footer">评分：9.5</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">追风筝的人</view>
        <view slot="footer">评分：9.1</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">我们仨</view>
        <view slot="footer">评分：9.0</view>
      </i-card></i-col>
</i-row>
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
      value1:1,
      current: 'tab1',
  }
  },
  methods:{
      
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
