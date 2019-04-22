<template>
<div>
 <i-panel title="借阅书籍信息">
    <i-input :value="value1" title="书籍名称" autofocus placeholder="请输入书籍名称" />
    <i-input-number value="value1" min="0" max="100" bindchange="handleChange1" />
    <i-input :value="value3 " title="借书日期" placeholder="请输入时间" />
    <i-input :value="value3 " title="还书日期" placeholder="请输入时间" />
</i-panel>
   <i-button type="success" inline i-class="ButCs">确认</i-button>
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

</style>
