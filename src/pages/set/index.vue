<template>
  <div>
    <i-panel title="信息推送设置">
    <i-cell-group>
    <i-cell title="个性推荐">
        <i-switch :value="switch1" @change="onChange" slot="footer"></i-switch>
    </i-cell>
    <i-cell title="新书推送">
        <i-switch :value="switch1" @change="onChange" slot="footer"></i-switch>
    </i-cell>
    <i-cell title="期刊推送">
        <i-switch :value="switch1" @change="onChange" slot="footer"></i-switch>
    </i-cell>
    <i-cell title="活动推送">
        <i-switch :value="switch1" @change="onChange" slot="footer"></i-switch>
    </i-cell>
    </i-cell-group>
</i-panel>
<i-panel title="个人信息">
  <view class="i-swipeout-demo-title">和actionsheet联合使用</view>
    <i-action-sheet visible="visible2" :actions="actions2" show-cancel bind:cancel="handleCancel2" bind:click="handleClickItem2" mask-closable="false">
        <view slot="header" style="padding: 16px">
            <view style="color: #444;font-size: 16px">确定吗？</view>
            <text>删除后无法恢复哦</text>
        </view>
    </i-action-sheet>
    <i-swipeout  i-class="i-swipeout-demo-item" operateWidth="180" unclosable="true" :toggle="toggle">
        <view slot="content">
            <view class="i-swipeout-image">
                <i-icon size="20" color="#FFFFFF" type="feedback_fill"></i-icon>
           </view>
           <view class="i-swipeout-des">
                <view class="i-swipeout-des-h2">第七个小矮人</view>
                <view class="i-swipeout-des-detail">乐观善良的7个小矮人原本过着简单快乐的生活，不料诅咒公主的巫婆利用小矮人进入.</view>
           </view>
        </view>
        <view slot="button" class="i-swipeout-demo-button-group" style="background:#2db7f5;">
            <view class="i-swipeout-demo-button" style="width:60px" bindtap="actionsTap"> <i-icon size="32" type="like_fill"></i-icon></view>
            <view class="i-swipeout-demo-button" style="width:60px" bindtap="actionsTap"><i-icon size="32" type="share_fill"></i-icon></view>
            <view class="i-swipeout-demo-button" style="width:60px" bindtap="actionsTap"><i-icon size="32" type="delete_fill"></i-icon></view>
        </view>
    </i-swipeout>
</i-panel>
  </div>
</template>

<script>


export default {
  data() {
    return {
     switch1 : false,
     visible2: false,
        //小程序没有refs，所以只能用动态布尔值控制关闭
        toggle : false,
        toggle2 : false,
        actions2: [
            {
                name: '删除',
                color: '#ed3f14'
            }
        ],
    }
  },
  methods: {
    onChange(event){
        const detail = event.detail;
        this.setData({
            'switch1' : detail.value
        })
        
    },
  }
}
</script>

<style>
.counter-warp {
  text-align: center;
  margin-top: 100px;
}
.home {
  display: inline-block;
  margin: 100px auto;
  padding: 5px 10px;
  color: blue;
  border: 1px solid blue;
}
</style>
