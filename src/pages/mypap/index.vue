<template>
<div>
 <i-card title="中国电化教育" extra="2019-01-03 17：29" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">中学生物学科“智慧学伴”平台的构建及其应用</view>
    <view slot="footer">王建 王聪 陈博杰 乔文军 刘颖</view>
</i-card>
 <i-card title="卡片标题" extra="额外内容" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
 <i-card title="卡片标题" extra="额外内容" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
 <i-card title="卡片标题" extra="额外内容" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
 <i-card title="卡片标题" extra="额外内容" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card> 
<i-card title="卡片标题" extra="额外内容" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
<i-page :current= current total="5" mode="pointer" @change="handleChange"></i-page>
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
        current: 1
  }
  },
  methods:{
      handleChange ( detail ) {
        const type = detail.type;
        if (type === 'next') {
         
                current=this.data.current + 1;
        } else if (type === 'prev') {
           
                current= this.data.current - 1;
        }
    }
  },
  created () {
    
  }
}
</script>

<style scoped>

</style>
