<template>
<div>
 <i-tabs :current="current" @change="handleChange">
    <i-tab key="tab1" title="自习室预约" ></i-tab>
    <i-tab key="tab2" title="书籍预约"></i-tab>
</i-tabs>
<div v-show="Show1">
<i-card title="3楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="3楼" extra="自习区" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class2.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">20个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="4楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">70个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="4楼" extra="自习区" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class2.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">20个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="5楼" extra="机房" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/电脑.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约机位">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="6楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="7楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="8楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="9楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="10楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="11楼" extra="阅览室" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/class1.png">
    <view slot="content">剩余位置</view>
    <view slot="footer">50个<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约自习室">
    <i-input  title="预订数量" autofocus placeholder="请输入座位数" i-class ="Icolor"/>
    <i-input  title="进入时间" placeholder="请输入时间" i-class ="Icolor" />
    <i-input  title="离开时间" placeholder="请输入时间" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
</div>
<div v-show="Show2">
<i-card title="围城" extra="7楼" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
    <view slot="content">可借本数</view>
    <view slot="footer">2本<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约书籍">
    <i-input  title="预订数量" autofocus placeholder="请输入要预约的书本数" i-class ="Icolor"/>
    <i-input  title="学号" placeholder="请输入学号" i-class ="Icolor" />
    <i-input  title="姓名" placeholder="请输入姓名" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="我们仨" extra="11楼" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
    <view slot="content">可借本数</view>
    <view slot="footer">3本<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约书籍">
    <i-input  title="预订数量" autofocus placeholder="请输入要预约的书本数" i-class ="Icolor"/>
    <i-input  title="学号" placeholder="请输入学号" i-class ="Icolor" />
    <i-input  title="姓名" placeholder="请输入姓名" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="西潮" extra="7楼" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
    <view slot="content">可借本数</view>
    <view slot="footer">2本<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约书籍">
    <i-input  title="预订数量" autofocus placeholder="请输入要预约的书本数" i-class ="Icolor"/>
    <i-input  title="学号" placeholder="请输入学号" i-class ="Icolor" />
    <i-input  title="姓名" placeholder="请输入姓名" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
<i-card title="人生" extra="7楼" thumb="cloud://ev-sonw-389539.6576-ev-sonw-389539/书本 (1).png">
    <view slot="content">可借本数</view>
    <view slot="footer">2本<i-button @click="toggleLeft2" type="primary" shape="circle" size="small">预约</i-button></view>
</i-card>
<i-drawer mode="left" :visible="showLeft2" mask-closable="false">
    <view class="demo-container">
    <i-panel title="预约书籍">
    <i-input  title="预订数量" autofocus placeholder="请输入要预约的书本数" i-class ="Icolor"/>
    <i-input  title="学号" placeholder="请输入学号" i-class ="Icolor" />
    <i-input  title="姓名" placeholder="请输入姓名" i-class ="Icolor"/>
</i-panel>
        <i-button @click="toggleLeft2" type="primary" size="small">确定</i-button>
    </view>
</i-drawer>
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
      Show1:true,
      Show2:false,
      current: 'tab1',
      showLeft2:false,
  }
  },
  methods:{
       handleChange (event) {
         let show
         console.log(event)
            this.current=event.mp.detail.key
            show=this.Show1
            this.Show1=this.Show2
            this.Show2=show
             console.log(this.Show1)
    },
    toggleLeft2() {
        this.showLeft2= !this.showLeft2;
    },
  },
  watch(){
      if(current==tab1){
              this.Show1=true
               Show2=false
            }
            if(current==tab2){
               Show2=true
              Show1=false
            }
  },
  created () {
    
  },
}
</script>

<style>

</style>
