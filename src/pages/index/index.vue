<template>
  <div>
     <i-notice-bar icon="systemprompt" loop>
    {{notice}}新书：钱钟书——《围城》
    </i-notice-bar>
    <i-input type="text" title="搜索" placeholder="请输入书籍名称 关键字" />
    <view class="userinfo">
  <view class="userinfo-avatar">
    <open-data type="userAvatarUrl"></open-data>
    </view>
    <open-data type="userNickName"></open-data>
      </view>
    <i-row>
    <i-col span="12" i-class="col-class"><i-card i-class="swidth" title="签到中心"></i-card></i-col>
  
    <i-col span="12" i-class="col-class1 "><i-card i-class="swidth" title="当前等级:LV3"></i-card></i-col>
 </i-row>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/1.png" />
        </i-grid-icon>
        <i-grid-label>我的书架</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/2.png" />
        </i-grid-icon>
        <i-grid-label>我的期刊</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/3.png" />
        </i-grid-icon>
        <i-grid-label>我的收藏</i-grid-label>
    </i-grid-item>
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/grid/活动.png" />
        </i-grid-icon>
        <i-grid-label>我的活动</i-grid-label>
    </i-grid-item>
</i-grid>
<i-panel title="每日排行">
  <i-row>
    <i-col span="8" i-class="col-class">  <view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/头像 女孩 (1).png">
        <view slot="content">snow</view>
        <view slot="footer">NO.1</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/头像 女孩.png">
        <view slot="content">snow</view>
        <view slot="footer">NO.2</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/头像 男孩.png">
        <view slot="content">snow</view>
        <view slot="footer">NO.1</view>
      </i-card></i-col>
</i-row>
</i-panel>
<i-panel title="每日推荐">
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
<i-panel title="图书导购">
      <view class="top-padding"></view>
        <i-row>
    <i-col span="8" i-class="col-class">  <view class="top-padding"></view>
      <i-card i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
      <i-card i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
      </i-card></i-col>
    <i-col span="8" i-class="col-class"><view class="top-padding"></view>
     <i-card i-class="top-padding" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
      </i-card></i-col>
</i-row>
      </i-panel>
   </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
      girds:['我的书架','我的期刊','我的收藏','我的活动'],
      notice: '2019年4月3日',
      motto: 'Hello miniprograme',
      userInfo: {
        nickName: 'mpvue',
        avatarUrl: 'http://mpvue.com/assets/logo.png'
      }
    }
  },

  components: {
    card
  },

  methods: {
    bindViewTap () {
      const url = '../logs/main'
      if (mpvuePlatform === 'wx') {
        mpvue.switchTab({ url })
      } else {
        mpvue.navigateTo({ url })
      }
    },
    clickHandle (ev) {
      console.log('clickHandle:', ev)
      // throw {message: 'custom test'}
    }
  },

  created () {
    // let app = getApp()
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
  width:150px;
  height:35px;
  background-color: #BFEFFF
}
</style>
