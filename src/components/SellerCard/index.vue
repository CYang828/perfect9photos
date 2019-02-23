<template>
  <view class="seller-card">
    <a :href="sellerUrl">
      <image :src="sellerImage" class="seller-card-image" />
    </a>
    <view class="seller-card-info">
      <lable class="seller-card-name">{{sellerName}}</lable>
      <label class="seller-card-price">{{sellerPrice}}</label>
    </view>
    <view class="seller-card-bonus">
      <view class="seller-card-bonus-line">
        <image class="seller-card-voucher" src="https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/line/vouncher.png" />
        <label class="seller-card-bonus-text seller-card-bonus-head">打卡进店赠甜品</label>
        <label class="seller-card-bonus-text seller-card-bonus-tail">5个优惠</label>
      </view>
      <view class="seller-card-bonus-line">
        <image class="seller-card-voucher" src="https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/line/vouncher.png" />
        <label class="seller-card-bonus-text seller-card-bonus-head">满58减20</label>
      </view>
      <van-button type="default" size="small" custom-class="seller-card-bonus-btn">领取</van-button>
    </view>
  </view>
</template>

<script>
export default {
  name: "SellerCard",
  props: {
    'sellerImage': {
      type: String
    },
    'sellerName': {
      type: String
    },
    'sellerPrice': {
      type: String
    },
    'sellerUrl': {
      type: String
    }
  }
}
</script>

<style>
.seller-card {
  padding: 0rpx;
}

.seller-card-image {
  width: 600rpx;
  height: 300rpx;
  border-radius: 20rpx;
}

.seller-card-voucher {
  width: 30rpx;
  height: 21rpx;
}

.seller-card-info {
  text-align: left;
}

.seller-card-name {
  margin-left: 90rpx;
  font-size: 30rpx;
  color: #000;
  font-weight: 600;
}

.seller-card-price {
  color: #686F7A;
  font-size: 20rpx;
  margin-left: 25rpx;
}

.seller-card-bonus {
  margin-top: 20rpx;
  text-align: left;
  margin-left: 90rpx;
}

.seller-card-bonus-line {
  margin-top: -20rpx;
}

.seller-card-bonus-text {
  font-size: 22rpx;
  color: #EA5252;
}

.seller-card-bonus-head {
  position: relative;
  top: -2rpx;
  margin-left: 8rpx;
}

.seller-card-bonus-tail {
  margin-left: 305rpx;
} 

.seller-card-bonus-btn {
  margin-left: 470rpx;
  background-color: #EA5252 !important;
  border-radius: 10rpx !important;
  margin-top: -40rpx;
}
</style>
