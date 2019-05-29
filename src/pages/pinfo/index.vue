<template>
<div>
 <i-panel title="读者基本信息">
    <i-input :value="value1"  title="姓名" autofocus placeholder="请输入名字" />
    <i-input :value="value2" type="number" title="学号" placeholder="请输入学号" />
    <i-input :value="value3 " title="年级专业" placeholder="请输入你的年级和专业" />
</i-panel>

<i-panel title="个性标签">
    <i-input :value="value5" placeholder="一句话描述自己" />
</i-panel>

<i-panel title="用户修改">
  <i-input :value="value1" @change="changeName($event)"  title="姓名" autofocus placeholder="请输入名字" />
    <i-input :value="value2" type="number" title="学号" placeholder="请输入学号" />
    <i-input :value="value3 " title="年级专业" placeholder="请输入你的年级和专业" />
    <i-input :value="value2" type="password" title="密码" placeholder="请输入新密码" />
</i-panel>
<i-panel>
  <i-button type="error" inline i-class="ButCs">确认修改</i-button>
   <i-button type="success" inline i-class="ButCs">取消修改</i-button>
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
     value1: '许明雪',
        value2: '201722111112064',
        value3: '闪光少女',
        value4: '输入框已禁用',
        value5: '',
        value6: '',
        value7: ''
  }
  },
  methods:{
      changeName (event) {
        console.log(event)
      if(event.target.detail.value==0){
      wx.showToast({
        title:"姓名不能为空",
        icon:'none'
         })
      }
    },
    
  },
  created () {
    
  }
}
</script>

<style>
.ButCs{
  margin:100px
}
</style>
