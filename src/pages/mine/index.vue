<template>
<div>
  <map
  id="map"
  longitude="114.34094"
  latitude="30.585014"
  scale="16"
  :controls="controls"
  @controltap="controltap"
  :markers="markers"
  @markertap="markertap"
  :polyline="polyline"
  bindregionchange="regionchange"
  show-location
  style="width: 100%; height: 500px;"
></map>
  </div>
</template>

<script>
import card from '@/components/card'

export default {
  data () {
    return {
       markers: [{
      iconPath: '/static/images/定位.png',
      id: 0,
      latitude: 30.584936,
      longitude: 114.341102,
      width: 50,
      height: 50
    }],
    polyline: [{
      points: [{
        longitude: 114.340792,
        latitude: 30.584971
      }, {
        longitude: 114.341385,
        latitude: 30.585014
      }],
      color: '#FF0000DD',
      width: 2,
      dottedLine: true
    }],
    controls: [{
      id: 1,
      iconPath: '/static/images/全局搜索.png',
      position: {
        left: 0,
        top: 300 - 50,
        width: 50,
        height: 50
      },
      clickable: true
    }]
    }
  },

  components: {
    card
  },

  methods: {
   regionchange(e) {
    console.log(e.type)
  },
  markertap(e) {
    console.log(e.markerId)
  },
  controltap(e) {
    console.log(e.controlId)
  }
    
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>


</style>
