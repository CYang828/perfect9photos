<template>
<view class="line-card">
  <view class="line-card-container">
    <!-- 点位模块 -->
    <view class="spot-items">
      <lable class="spot-items-title">本路线包含6个打卡点位</lable>
      <!-- <van-row custom-class="spot-items-tag">
        <slide speed="100">
          <van-col custom-class="spot-items-tag-col">
            <van-tag @click="onClick(1)" custom-class="spot-item-tag">1号</van-tag>
          </van-col>
          <van-col custom-class="spot-items-tag-col">
            <van-tag @click="onClick(2)" custom-class="spot-item-tag spot-item-tag-gap">2号</van-tag>
          </van-col>
          <van-col custom-class="spot-items-tag-col">
            <van-tag @click="onClick(3)" custom-class="spot-item-tag spot-item-tag-gap">3号</van-tag>
          </van-col>
          <van-col custom-class="spot-items-tag-col">
            <van-tag @click="onClick(5)" custom-class="spot-item-tag spot-item-tag-gap">5号</van-tag>
          </van-col>
          <van-col custom-class="spot-items-tag-col">
            <van-tag @click="onClick(7)" custom-class="spot-item-tag spot-item-tag-gap">7号</van-tag>
          </van-col>
          <van-col custom-class="spot-items-tag-col">
            <van-tag @click="onClick(8)" custom-class="spot-item-tag spot-item-tag-gap">8号</van-tag>
          </van-col>
        </slide>
      </van-row> -->
      <view class="spot-items-checkpoints">
        <van-row>
          <view class="spot-item-checkpoint spot-item-checkpoint-checked ">
            <view class="spot-item-checkpoint-text-offset">
              <label class="spot-item-checkpoint-text">1号</label>
            </view>
            <view class="spot-item-checkpointed-gap">
              <label class="spot-item-checkpoint-text">已打卡</label>
            </view>
          </view>
          <view class="spot-item-checkpoint spot-item-checkpoint-checked spot-item-checkpoint-left">
            <view class="spot-item-checkpoint-text-offset">
              <label class="spot-item-checkpoint-text">2号</label>
            </view>
            <view class="spot-item-checkpointed-gap">
              <label class="spot-item-checkpoint-text">已打卡</label>
            </view>
          </view>
          <view class="spot-item-checkpoint spot-item-checkpoint-left">
            <view class="spot-items-checkpoints-line-offset-unchecked ">
              <label class="spot-item-checkpoint-text">3号</label>
            </view>
          </view>
          <view class="spot-item-checkpoint spot-item-checkpoint-selected spot-item-checkpoint-left">
            <view class="spot-items-checkpoints-line-offset-unchecked ">
              <label class="spot-item-checkpoint-text">4号</label>
            </view>
          </view>
        </van-row>

        <van-row custom-class="spot-items-checkpoints-line-offset">
          <view class="spot-item-checkpoint">
            <view class="spot-items-checkpoints-line-offset-unchecked ">
              <label class="spot-item-checkpoint-text">5号</label>
            </view>
          </view>
          <view class="spot-item-checkpoint spot-item-checkpoint-left">
            <view class="spot-items-checkpoints-line-offset-unchecked ">
              <label class="spot-item-checkpoint-text">6号</label>
            </view>
          </view>
        </van-row>
      </view>

      <view class="spot-detail">
        <lable class="spot-detail-title">详情</lable>
        <view>
          <view class="spot-detail-checkpoint-title">
            <label>4号点位</label>
          </view>
          <view class="spot-detail-checkpoint-info">
            <image class="spot-detail-checkpoint-address-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/location.png" />
            <label class="spot-detail-checkpoint-address">广东省梅州市梅州县xx区xxxx街道xx号</label>
          </view>
          <van-row>
            <van-button type="default" size="small" custom-class="spot-detail-checkpoint-direction-btn">导航</van-button>
            <van-button type="default" size="small" custom-class="spot-detail-checkpoint-check-btn">打卡</van-button>
          </van-row>
        </view>
      </view>
    </view>

    <realtime-view :viewImage1="data[spotIndex].viewImage1"
    :viewImage1Time="data[spotIndex].viewImage1Time"
    :viewImage2="data[spotIndex].viewImage2"
    :viewImage2Time="data[spotIndex].viewImage2Time"
    :viewImage3="data[spotIndex].viewImage3" />

    <!-- <spot-detail
    :title="data[spotIndex].title"
    :viewImage1="data[spotIndex].viewImage1"
    :viewImage1Time="data[spotIndex].viewImage1Time"
    :viewImage2="data[spotIndex].viewImage2"
    :viewImage2Time="data[spotIndex].viewImage2Time"
    :viewImage3="data[spotIndex].viewImage3"
    :viewImage3Time="data[spotIndex].viewImage3Time"
    :info="data[spotIndex].info"
    :image="data[spotIndex].image"
    :detail="data[spotIndex].detail"
    :address="data[spotIndex].address"
    :price="data[spotIndex].price"
    :phone="data[spotIndex].phone"
    :way="data[spotIndex].way"
    :open="data[spotIndex].open" /> -->
  </view>
  <spot-arounding />
</view>
</template>

<script>
import slide from '@/components/mpvue-slide/mpvue-slide.vue'
import SpotDetail from '@/components/SpotDetail/index.vue'
import RealtimeView from '@/components/RealtimeView/index.vue'
import SpotArounding from '@/components/SpotArounding/index.vue'

export default {
  name: "LineDesc",
  data () {
    return {
      spotIndex: 1,
      data: {
        1: {title: "围龙屋星园酒家",
            viewImage1: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot1-1.png",
            viewImage1Time: "1月6日 08:00",
            viewImage2: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot1-2.png",
            viewImage2Time: "1月6日 13:00",
            viewImage3: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot1-3.png",
            viewImage3Time: "1月6日 19:00",
            info: "当地老店，位于有一百多年历史的客家围屋内，环境古色古香。主打正宗的梅州客家菜，推荐五叶神汤、客家酿豆腐、一品豆腐、苦笋煲、凉瓜牛肉、盐焗鸡、酸辣大肠等，还可配上一杯甜甜暖暖的客家酿酒。服务也较热情。",
            image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot1.png",
            address: "地址：梅州梅江区三角镇富奇路41号承德楼内（近剑英公园）",
            price: "费用：人均70元",
            phone: "电话： 2331315",
            way: "到达交通：乘1、12、25路公交车在三角地站下车即到",
            open: "开放时间: 11:00-20:00"},
        2: {title: "万秋楼",
            viewImage1: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot2-1.png",
            viewImage1Time: "1月6日 08:00",
            viewImage2: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot2-2.png",
            viewImage2Time: "1月6日 13:00",
            viewImage3: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot2-3.png",
            viewImage3Time: "1月6日 20:00",
            info: "由华侨大宅改造而成，环境非常有客家特色，古色古香，可从中了解客家建筑风俗及饮食文化。客家菜味道地道，还可品尝自家酿的客家娘酒，入口香醇。厅堂还放有大茶几，有兴致的话可在此冲茶，且有陈年普洱提供。",
            image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot2.png",
            address: "地址：梅州市梅县新城办事处扶外村98号（近新城加油城）",
            price: "费用：人均55元",
            phone: "电话： 2530288",
            way: "到达交通：乘12、25路等公交车在梅雁中学站下车可达",
            open: "20:30停止下单"},
        3: {title: "梅州好吃腌面全猪汤",
            viewImage1: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot3-1.png",
            viewImage1Time: "1月6日 08:00",
            viewImage2: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot3-2.png",
            viewImage2Time: "1月6日 13:00",
            viewImage3: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot3-3.png",
            viewImage3Time: "1月6日 20:00",
            info: "老字号餐馆，招牌腌面的猪油香味诱人，面条也有嚼劲，配个全猪汤最好，有猪肚和猪心等丰富食材，不吃猪杂的也可选择吃牛肉汤。分量实在，吃宵夜生意特好。",
            image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot3.png",
            address: "地址：梅州市梅江区江南三横街新中路中段达兴全猪汤-总店（五粮液隔壁）",
            price: "费用：人均15元 ",
            phone: "电话： 15986499885 ",
            way: "到达交通：乘7、19路等公交车在人才市场站下车可达",
            open: "开放时间:  全天"},
        5: {title: "金苑酒家",
            viewImage1: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot5-1.png",
            viewImage1Time: "1月6日 08:00",
            viewImage2: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot5-2.png",
            viewImage2Time: "1月6日 13:00",
            viewImage3: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot5-3.png",
            viewImage3Time: "1月6日 20:00",
            info: "已开业30多年的老店，主打正宗、传统客家菜式，店内也是清一色的客家装修风格。自然菜式也是让人大饱口福，推荐炸丝瓜，味道不同寻常，保留了丝瓜的润滑和炸物的脆口，调好味的肉末夹在中间更是将丝瓜的清甜凸显得淋漓尽致。",
            image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot5.png",
            address: "地址：梅州市梅江区金苑小区",
            price: "费用：人均70-75元",
            phone: "电话： 2298289",
            way: "到达交通：乘5、12、18、27路公交车在渡江津站下车可达",
            open: "开放时间:  9:00-20:00"},
        7: {title: "亚巫肉丸",
            viewImage1: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot7-1.png",
            viewImage1Time: "1月6日 08:00",
            viewImage2: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot7-2.png",
            viewImage2Time: "1月6日 13:00",
            viewImage3: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot7-3.png",
            viewImage3Time: "1月6日 20:00",
            info: "梅州三十多年的老字号小吃店，还曾被电视节目推荐。推荐西施炒米粉、肉丸汤。",
            image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot7.png",
            address: "地址：梅州市梅江区江边路5号店，东山桥，往望江楼方向100米（原百花洲公厕对面，原中山街）",
            price: "费用：人均20元",
            phone: "电话： 13411288893",
            way: "到达交通：乘3、4路空调、15、20路等公交车在江边路站下车可达",
            open: ""},
        8: {title: "叶家饭店",
            viewImage1: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot8-1.png",
            viewImage1Time: "1月6日 08:00",
            viewImage2: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot8-2.png",
            viewImage2Time: "1月6日 13:00",
            viewImage3: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot8-3.png",
            viewImage3Time: "1月6日 20:00",
            info: "近叶剑英故居，很实在的家常菜馆，无论肉和青菜材料都很新鲜，味道也正宗。现宰的走地鸡肉质香嫩，自酿娘酒美味醇香。为家庭经营，态度亲切，价格实惠。",
            image: "cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/line/spot8.png",
            address: "地址：梅州市梅县223省道",
            price: "费用：人均50元",
            phone: "电话： 2825253",
            way: "到达交通：乘10、17路等公交车在剑英纪念园站下车可达",
            open: "开放时间:  8:00-20:00"},
      }
    }
  },
  components: {
    slide,
    SpotDetail,
    RealtimeView,
    SpotArounding
  },
  methods: {
    onClick(index) {
      this.spotIndex = index
    }
  }
}
</script>

<style>
.line-card-container {
  margin-left: 30rpx;
  padding: 0 !important;
  margin-top: 0 !important;
}

.spot-items {
  text-align: middle;
}

.spot-items-title {
  font-size: 34rpx;
  font-weight: 700;
  color: #000;
  margin-left: -15rpx;
}

.spot-items-tag {
  margin-right: 0 !important;
  display: inline;
  white-space: nowrap; 
  overflow: hidden;
}

.spot-items-checkpoints {
  margin-top: 35rpx;
}


.spot-item-checkpoint {
  position: inline-block;
  float: left;
  border-radius: 50% !important;
  border: solid #000 1px !important;
  height: 135rpx;
  width: 135rpx;
}

.spot-items-checkpoints-line-offset {
  margin-top: 20rpx;
}

.spot-items-checkpoints-line-offset-unchecked {
  position: relative;
  top: 40rpx;
}

.spot-item-checkpoint-left {
  margin-left: 44rpx;
}

.spot-item-checkpoint-checked {
  background-color: #FF8181;
  border: solid #FF8181 1px !important;
  color: #fff !important;
}

.spot-item-checkpoint-selected {
  border: solid #FF8181 2px !important;
}

.spot-item-checkpoint-text {
  font-size: 25rpx;
}

.spot-item-checkpoint-text-offset {
  position: relative;
  top: 28rpx;
}

.spot-item-tag {
  width: 136rpx;
  height: 60rpx;
  padding: 0 !important;
  display: flex !important;
  align-items: center;
  justify-content: center; 
  border-radius: 8rpx !important;
  background-color: #EEF1F6 !important;
  color: #838386 !important;
  margin-top: 15rpx;
  font-size: 25rpx !important;
}

.spot-items-tag-col {
  display: inline-block;
}

.spot-item-tag-gap {
  margin-left: 18rpx;
}

.spot-item-tag-selected {
  background-color: #EAEDF4 !important;
  color: #28272C !important;
  font-weight: 600;
}

.spot-detail {
  margin-left: -15rpx !important;
  margin-top: 30rpx;
}

.spot-detail-title {
  text-align: center;
  color: #686F7A;
  font-size: 28rpx;
  margin-left: -15rpx
}

.spot-detail-checkpoint-info {
  text-align: center;
}

.spot-detail-checkpoint-title
{
  margin-top: 20rpx;
  color: #FF8181;
  font-size: 30rpx;
  font-weight: 800;
  margin-left: -15rpx;
}

.spot-detail-checkpoint-address {
  color: #686F7A;
  font-size: 25rpx;
  margin-left: 8rpx;
}

.spot-detail-checkpoint-direction-btn {
  background-color: #686F7A !important;
  margin-right: 20rpx;
  color: #fff !important; 
  margin-top: 20rpx;
  border-radius: 10rpx !important;
}

.spot-detail-checkpoint-check-btn {
  background-color: #FF8181 !important;
  margin-right: 20rpx;
  color: #fff !important;  
  margin-top: 20rpx;
  border-radius: 10rpx !important;
}

.spot-detail-checkpoint-address-icon {
  width: 20rpx;
  height: 28rpx;
  position: relative;
  top: 6rpx;
}

.spot-detail-realtime {
  padding-bottom: 20rpx;
  border-bottom: solid 2rpx #F5F3F1;
}

.spot-detail-realtime-title {
  text-align: left;
  margin-top: 30rpx;
  margin-left: -15rpx;
  font-weight: 800;
}

.spot-detail-realtime-text {
  font-size: 40rpx;
  font-weight: 500;
}

.spot-detail-realtime-images {
  margin-top: 30rpx;
}

.spot-detail-realtime-image {
  display: inline-block;
  width: 220rpx;
  height: 180rpx;
}

.spot-detail-realtime-image-gap {
  margin-left: 20rpx;
}

.spot-detail-realtime-times {
  text-align: left;
}

.spot-detail-realtime-item {
  width: 220rpx;
  text-align: left;
}

.spot-detail-realtime-item-gap {
  margin-left: 20rpx;
}

.spot-detail-realtime-time {
  color: #838386;
  font-size: 24rpx;
  position: relative;
  top: -10rpx;
}

.spot-detail-realtime-time-gap {
  margin-left: 30rpx;
}

.spot-item-checkpointed-gap {
  margin-top: 10rpx !important;
}
</style>
