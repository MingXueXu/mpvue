<template>
<div>
 
    <i-panel title="我的收藏">
      <view>
        <i-card i-class="split" v-for="item in list" :key="item" :extra="item.type" :thumb="item.img">
            <view slot="content">{{item.content}}</view>
            <view slot="footer">{{item.time}}</view>
        </i-card>
      </view>
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
     list: []
    }
  },
onLoad(item){
this.list=require('@/data/'+item.type+'.json')
 console.log(this.list)
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
