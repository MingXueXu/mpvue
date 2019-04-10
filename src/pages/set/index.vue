<template>
  <div>
    <i-panel title="信息推送设置">
    
</i-panel>
  </div>
</template>

<script>


export default {
  data: {
     switch1 : false
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
