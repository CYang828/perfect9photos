<template>
  <view class="spot-arounding">
    <label class="spot-arounding-title">点位周边好去处</label>
    <view class="spot-arounding-title-gap">
      <seller-card :sellerImage="'https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/line/seller1.png'" 
                   :sellerName="'情人湖餐厅'" :sellerPrice="'人均90元'"
                   :sellerUrl="'/pages/detail/main'" />
      <view class="spot-arounding-item-gap"></view>
      <seller-card :sellerImage="'https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/line/seller2.png'" 
                   :sellerName="'情人湖餐厅'" :sellerPrice="'人均90元'" 
                   :sellerUrl="'/pages/detail/main'" />
      <view class="spot-arounding-item-gap"></view>
      <seller-card :sellerImage="'https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/line/seller3.png'" 
                   :sellerName="'情人湖餐厅'" :sellerPrice="'人均90元'" 
                   :sellerUrl="'/pages/detail/main'" />
      <view class="spot-arounding-item-gap"></view>
      <seller-card :sellerImage="'https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/line/seller4.png'" 
                   :sellerName="'情人湖餐厅'" :sellerPrice="'人均90元'" 
                   :sellerUrl="'/pages/detail/main'" />
    </view>
  </view>
</template>

<script>
import SellerCard from '@/components/SellerCard/index.vue'

export default {
  name: "SpotArounding",
  components: {
    SellerCard
  }
}
</script>

<style>
.spot-arounding {
  margin: 0;
}

.spot-arounding-title {
  font-weight: 800;
  text-align: center;
  font-size: 28rpx;
  color: #000;
}

.spot-arounding-title-gap {
  margin-top: 30rpx;
}

.spot-arounding-item-gap {
  margin-top: 30rpx;
}
</style>
