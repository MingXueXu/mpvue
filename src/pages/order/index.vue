<template>
<div>
 <i-tabs :current="current" @change="handleChange">
    <i-tab key="tab1" title="书籍预约"></i-tab>
    <i-tab key="tab2" title="自习室预约"></i-tab>
</i-tabs>
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
      current: 'tab1',
  }
  },
  methods:{
       handleChange (event) {
         console.log(event.mp.detail.key)
            this.current=event.mp.detail.key
    },
  },
  created () {
    
  }
}
</script>

<style>

</style>
