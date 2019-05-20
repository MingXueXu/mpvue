<template>
<div>
  <i-notice-bar>
    2019年5月20日，湖北大学举行读书交流会
</i-notice-bar>

  <swiper
      :indicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
      style="height:200px"
    >
    <block v-for="item in imgUrls" :key="item">
      <swiper-item>
        <image :src="item" style="width:100%;"/>
      </swiper-item>
    </block>
  </swiper>
<view class="caption-wrap">
    <text class="caption-title">近期活动</text>
    <i-collapse name="name">
        <i-collapse-item title="我馆荣获湖北大学教职工羽毛球团体比赛三等奖" name="name1">
            <view slot="content">
               日前，为丰富我校教职工业余生活，促进教职工的沟通交流，增强教职工身体素质，由校工会组织的全校教职工羽毛球团体比赛在三号体育馆举行。我馆积极响应，精心挑选出一支精英队伍参加比赛。比赛中，我馆运动员防攻结合、斗智斗勇、扣杀、救球等精彩场面持续不断，淋漓尽致发挥出队员们的团结拼搏，奋力相争，永不言弃的精神，最终获得湖北大学教职工羽毛球团体比赛三等奖。
            </view>
        </i-collapse-item>

        <i-collapse-item title="第二届湖北大学中华经典美文诵读大赛在我馆举行" name="name2">
            <view slot="content" i-class-content="green-text">
               5月8日下午，湖北大学第二届中华经典美文诵读大赛决赛在图书馆6楼会议室举行。19件优秀作品的20位诵读者在此进行精彩竞演。

比赛现场，参赛选手们或深情款款，或激情澎湃，或娓娓道来，演绎了《岳阳楼记》《就是那一只蟋蟀》《将进酒》《胡琏将军的绝别书》《致橡树》《再别康桥》《相信未来》等古今中华经典诗文名篇，给现场观众带来了一场视听盛宴，赢得了阵阵掌声。
            </view>
            </i-collapse-item>
          
             <i-collapse-item title="世界读书日，我馆举办作家尔容新书《伍子胥》校园分享会" name="name2">
            <view slot="content" i-class-content="green-text">
               4月23日晚7点，作家尔容新书长篇历史小说《伍子胥》校园分享会在会议中心思诚厅举行。知名文学评论家吴平安老师、湖北大学文学院院长刘川鄂教授、历史文化学院党委书记刘明达、图书馆副馆长骆晓曙、历史文化学院党委副书记郭仿兰、历史文化学院副教授曾育荣等到场祝贺。现场近百名师生读者参与。
            </view>
            </i-collapse-item>
          
             <i-collapse-item title="唱响中华诗词经典，刘冬颖教授做客“书香琴韵”大讲堂" name="name2">
            <view slot="content" i-class-content="green-text">
                4月19日下午，黑龙江大学文学院博士生导师刘冬颖教授做客“书香琴韵”大讲堂第33讲，为我校师生带来了一场题为《唱响中华诗词经典》的精彩学术讲座，近百名师生读者参与。
            </view>
             </i-collapse-item>
             
             <i-collapse-item title="湖北大学第八届大学生创意读书节系列活动举行" name="name2">
            <view slot="content" i-class-content="green-text">
                4月17日，我校第八届“大学生创意读书节”系列活动正式启动。下午两点半，“十大读者之星”颁奖仪式在图书馆二楼举行。宣传部部长刘靖君、教务处副处长殷云飞、学工处主任张珣和图书馆馆长刘刚、图书馆党总支书记何应华等相关领导出席活动。
            </view>
        </i-collapse-item>

        <i-collapse-item title="党总支扩大会（理论学习中心组）专题学习讨论RFID" name="name3">
            <view slot="content">
               3月27日上午图书馆总支委（理论学习中心组）召开扩大会，专题学习智慧图书馆建设（RFID系统建设），会议由总支书记何应华同志主持，馆长刘刚、副馆长骆晓曙、四位支部书记及7位部门主任、党务秘书参加了会议。
            </view>
        </i-collapse-item>
    </i-collapse>
</view>
  <i-divider content="我也是有底线的哟" color="#2d8cf0" lineColor="#2d8cf0"></i-divider>
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
      imgUrls: [
        'http://lib.hubu.edu.cn/__local/D/7D/40/5F49483FCAF7618B97E9B7921F4_2AE8D7B9_CC5F6.png',
        'http://lib.hubu.edu.cn/__local/F/9A/8D/119B34B058589951181625A779D_4C8288CD_62F7B.png',
        'http://lib.hubu.edu.cn/__local/0/9A/63/909E397D1EED8910849D4652065_74A49A9C_6AC6D.jpg'
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 5000,
      duration: 1000,
       name: 'name1'
    }
  },
  methods:{
     
  },
  created () {
    
  }
}
</script>

<style scoped>

</style>
