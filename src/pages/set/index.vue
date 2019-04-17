<template>
  <div>
    <i-panel>
    <i-cell-group>
    <i-cell title="个人信息修改" is-link url="/src/pages/pinfo/index"></i-cell>
    <i-cell title="在线借阅信息" is-link url="/src/pages/index/index"></i-cell>
</i-cell-group>
    </i-panel>
    <i-panel title="信息推送设置">
    <i-cell-group>
    <i-cell title="个性推荐">
        <switch checked slot="footer"></switch>
    </i-cell>
    <i-cell title="新书推送">
       <switch checked slot="footer"></switch>
    </i-cell>
    <i-cell title="期刊推送">
       <switch checked slot="footer"></switch>
    </i-cell>
    <i-cell title="活动推送">
        <switch checked slot="footer"></switch>
    </i-cell>
    </i-cell-group>
</i-panel>
<i-panel title="个人信息设置">
    <i-cell-group>
    <i-cell title="显示我的定位信息">
        <switch checked slot="footer"></switch>
    </i-cell>
    <i-cell title="显示我的借阅书籍情况">
        <switch checked slot="footer"></switch>
    </i-cell>
    </i-cell-group>
</i-panel>
  </div>
</template>

<script>


export default {
  data() {
    return {
    
  }},
  methods: {
    
  }
}
</script>

<style>

</style>
