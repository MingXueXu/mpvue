<template>
  <div>
    <i-panel title="信息推送设置">
    <view style="padding: 15px;">
      <i-cell-group>
    <i-cell title="基本用法">
        <i-switch  @change="onChange" slot="footer"></i-switch>
    </i-cell>
    <i-cell title="自定义内容">
        <i-switch  size="large" @change="onChange" slot="footer">
            <view slot="open">开启</view>
            <view slot="close">关闭</view>
        </i-switch>
    </i-cell>
    <i-cell title="图标">
        <i-switch @change="onChange" slot="footer">
            <i-icon type="right" slot="open"></i-icon>
            <i-icon type="close" slot="close"></i-icon>
        </i-switch>
    </i-cell>
</i-cell-group></view>
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
