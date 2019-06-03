<template>
<div>
 <i-card title="中国电化教育" extra="2019年1月3日" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">中学生物学科“智慧学伴”平台的构建及其应用</view>
    <view slot="footer">王建 王聪 陈博杰 乔文军 刘颖</view>
</i-card>
 <i-card title="现代教育技术" extra="2019年5月15日" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">教育技术工作者专业情意的时代表征</view>
    <view slot="footer">李琼 焦建利</view>
</i-card>
 <i-card title="中国电化教育" extra="2019年1月3日" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">基于网络平台的语文关键能力评价</view>
    <view slot="footer">李倩 孙名谣</view>
</i-card>
 <i-card title="电化教育研究" extra="2018年4月12日" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">SPOC平台下指向深度教学模式构建</view>
    <view slot="footer">孙晓娟 吕立杰</view>
</i-card>
 <i-card title="现代教育技术" extra="2018年5月15日" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">舒鑫城与电化教育学“中国化”的早期尝试</view>
    <view slot="footer">陆秀清</view>
</i-card> 
<i-card title="教育研究" extra="2018年3月15日" full=true thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/报纸.png">
    <view slot="content">教育技术：研究进展及反思</view>
    <view slot="footer">熊才平 戴红斌 葛军</view>
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
