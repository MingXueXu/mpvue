<template>
<div>
 <i-panel title="读者基本信息">
    <i-input :value="value1" title="姓名" autofocus placeholder="请输入名字" />
    <i-input :value="value2" type="number" title="学号" placeholder="请输入学号" />
    <i-input :value="value3 " title="年级专业" placeholder="请输入你的年级和专业" />
</i-panel>

<i-panel title="个性标签">
    <i-input :value="value5" placeholder="一句话描述自己" />
</i-panel>

<i-panel title="用户修改">
  <i-input :value="value1" title="姓名" autofocus placeholder="请输入名字" />
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
     value1: '',
        value2: '',
        value3: '',
        value4: '输入框已禁用',
        value5: '',
        value6: '',
        value7: ''
  }
  },
  methods:{
       handleChange (detail) {
        this.setData({
            current: detail.key
        });
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
