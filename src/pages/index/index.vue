<template>
  <div>
     <i-notice-bar icon="systemprompt" loop>
    今日新书：钱钟书——《围城》
    </i-notice-bar>
    <i-input type="text" title="搜索" placeholder="请输入书籍名称 关键字" />
    <view class="userinfo">
    <view class="userinfo-avatar">
    <open-data type="userAvatarUrl"></open-data>
    </view>
    <open-data type="userNickName"></open-data>
    </view>
    <i-row>
    <i-col span="12" i-class="col-class"><i-icon type="activity" size="28" color="#1296db" />签到中心</i-col>
    <i-col span="12" i-class="col-class ">当前等级:LV3<i-icon type="collection" size="28" color="#1296db" /></i-col>
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
      <view class="top-padding"></view>
      <i-card  i-class="top-padding" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">snow</view>
        <view slot="footer">NO.1</view>
      </i-card>
</i-panel>
<i-panel title="每日推荐">
      <view class="top-padding"></view>
      <i-card i-class="top-padding" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">明朝那些事</view>
        <view slot="footer">评分：9.5</view>
      </i-card>
</i-panel>
<i-panel title="图书导购">
      <view class="top-padding"></view>
      <i-card i-class="top-padding" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
        <view slot="content">内容不错</view>
        <view slot="footer">尾部内容</view>
      </i-card>
      </i-panel>
   </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
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
.top-padding {
  padding-top: 50rpx;
}
.userinfo {
position: relative;
width: 750rpx;
height: 320rpx;
color: #666;
display: flex;
flex-direction: column;
align-items: center;
}
 
.userinfo-avatar {
overflow:hidden;
display: block;
width: 160rpx;
height: 160rpx;
margin: 20rpx;
margin-top: 50rpx;
border-radius: 50%;
border: 2px solid #fff;
box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
}
div>>>.col-class{
  padding-right: 0pt;
}
</style>
