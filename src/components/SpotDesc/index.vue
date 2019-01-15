<template>
<!-- 景点介绍模块 -->
<view class="desc">
  <view slot="title" class="desc-title">
    <view class="desc-title-head">
      <image mode="scaleToFill" class="desc-title-head-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/location.png" />
      <label class="desc-title-head-text">梅州</label>
    </view>
    <view class="desc-title-tail">
      <image mode="scaleToFill" class="desc-title-tail-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/sun.png" />
      <label class="desc-title-tail-text">25°</label>
    </view>
  </view>
  <label class="desc-info">梅州是国家历史文化名城，是我国汉族客家人最集中的聚居地，素有“世界客都”之称。梅州市自古以来就有“梅花之乡”的称谓，域内多见古梅。</label>
  <!-- <image mode="scaleToFill" class="desc-spot-map" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/spot-map.png" /> -->
  <map class="desc-spot-map" subkey="U5FBZ-YMM6G-5OJQY-IORMX-YKISV-TCB4Z"
  longitude="116.12"
  latitude="24.28"
  scale=13 />
</view>
</template>

<script>
export default {
  name: "SpotDesc"
}
</script>

<style>
.desc {
  margin-left: 30rpx;
  margin-right: 30rpx;
  margin-top: 30rpx;
  padding-bottom: 30rpx;
  border-bottom: solid 2rpx #F5F3F1;
}

.desc-title {
  text-align: left;
}

.desc-title-head {
  display: inline-block;
}

.desc-title-tail {
  display: inline-block;
  margin-left: 410rpx;
}

.desc-title-head-icon {
  width: 40rpx;
  height: 56rpx;
}

.desc-title-head-text {
  position: relative;
  top: -4rpx;
  font-size: 60rpx;
  font-weight: 800;
  margin-left: 8rpx;
}

.desc-title-tail-icon {
  width: 60rpx;
  height: 60rpx;
}

.desc-title-tail-text {
  position: relative;
  top: -16rpx;
  margin-left: 4rpx;
  font-size: 30rpx;
  font-weight: 400;
}

.desc-info {
  margin-top: 10rpx;
  font-size: 26rpx;
  color: #838386;
  text-align: left;
  display: block;
}

.desc-spot-map {
  margin-top: 30rpx;
  width: 690rpx;
  height: 350rpx; 
}
</style>
