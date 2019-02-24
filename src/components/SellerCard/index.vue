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
      <view class="seller-card-bonus-line seller-card-bonus-offset">
        <label class="seller-card-bonus-text ">......</label>
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
  margin-left: 68rpx;
  width: 560rpx;
  background-color:#fff;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.1);
  border-radius: 20rpx;
  padding:20rpx 30rpx;

}

.seller-card-image {
  width: 560rpx;
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
  margin-left: 20rpx;
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
}

.seller-card-bonus-line {
  margin-left: 20rpx;
  margin-top: -20rpx;
}

.seller-card-bonus-offset {
  margin-top: -30rpx;
}

.seller-card-bonus-text {
  font-size: 22rpx;
  color: #FF8181;
}

.seller-card-bonus-head {
  position: relative;
  top: -2rpx;
  margin-left: 8rpx;
}

.seller-card-bonus-tail {
  margin-left: 255rpx;
} 

.seller-card-bonus-btn {
  margin-left: 450rpx;
  background-color: #FF8181 !important;
  border-radius: 10rpx !important;
  margin-top: -40rpx;
  color: #fff !important;
  height: 50rpx !important;
}
</style>
