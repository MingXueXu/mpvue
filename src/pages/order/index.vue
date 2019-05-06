<template>
<div>
 <i-tabs :current="current" @change="handleChange">
    <i-tab key="tab1" title="书籍预约"></i-tab>
    <i-tab key="tab2" title="自习室预约"></i-tab>
</i-tabs>
<div v-show="Show1">
 <i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
<i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
<i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
</div>
<div v-show="Show2">
 <i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
<i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
<i-card title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
</div>
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
      Show1:true,
      Show2:false,
      current: 'tab1',
  }
  },
  methods:{
       handleChange (event) {
         console.log(event)
            this.current=event.mp.detail.key
    },
  },
  created () {
    
  }
}
</script>

<style>

</style>
