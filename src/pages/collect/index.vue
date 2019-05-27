<template>
<div>
 <div>
    <i-panel title="我的收藏">
      <view>
        <i-card i-class="split" v-for="item in recommand" :key="item" :extra="item.name" :thumb="item.img">
            <view slot="content">{{item.content}}</view>
            <view slot="footer">{{item.time}}</view>
        </i-card>
      </view>
    </i-panel>
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
      recommand: []
    }
  },

  onLoad (option){
    console.log(option.type)
    this.recommand = require('@/collect/' + option.type + '.json')
  },

  created () {
    
  }
}
</script>

<style scoped>
div >>> .split {
  margin-bottom: 10pt;
}
</style>
