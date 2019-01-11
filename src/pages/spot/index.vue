<template>
<view class="container">
  <!-- 封面模块 -->
  <view>
    <video 
    class="video-cover" 
    src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/video/cover.mp4" 
    objectFit="cover"
    poster="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/cover.png" />
  </view>

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
    <image mode="scaleToFill" class="desc-spot-map" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/spot-map.png" />
  </view>
    
  <!-- 路线列表 -->
  <view class="line-items">
    <view class="line-items-head">
      <label class="line-items-head-text">九图攻略</label>
    </view>
    <!-- 过滤器 -->
    <view class="line-items-filter">
      <van-row>
        <van-col>
          <view class="line-items-filter-condition">
            <span class="line-items-filter-text">全部线路</span>
            <image class="arrow-down" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/arrow-down-gray.png" />
          </view>
        </van-col>
        <van-col>
          <view class="line-items-filter-condition">
            <span class="line-items-filter-text line-items-filter-gap line-items-filter-selected">热度排序</span>
            <image class="arrow-down" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/arrow-down-black.png" />
          </view>
        </van-col>
        <van-col>
          <view>
            <label class="line-items-filter-text line-items-filter-gap">所有时间</label>
            <image class="arrow-down" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/arrow-down-gray.png" />
          </view>
        </van-col>
      </van-row>
    </view>
    
    <!-- 路线item -->
    <view>
      <van-row>
        <van-col custom-class="line-item">
          <a href="/pages/line/main">  
            <image class="line-item-image" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line1.png" />
          </a>
          <lable class="line-item-desc-title">3天吃遍梅州美食</lable>
          <label class="line-item-desc-info">预算2000，吃货福利！</label>
          <view class="line-item-desc-footer">
            <image class="line-item-desc-like" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
            <label class="line-item-desc-like-count">29</label>
            <image class="line-item-desc-hotism" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/hot.png" />
            <label class="line-item-desc-hotism-count">2068</label>
          </view>
        </van-col>
        <van-col>
          <van-col custom-class="line-item line-item-gap">
            <image class="line-item-image" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line2.png" />
            <lable class="line-item-desc-title">梅州周边名胜打卡</lable>
            <label class="line-item-desc-info">一站解锁珠三角！</label>
            <view class="line-item-desc-footer">
              <image class="line-item-desc-like" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
              <label class="line-item-desc-like-count">25</label>
              <image class="line-item-desc-hotism" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/hot.png" />
              <label class="line-item-desc-hotism-count">1937</label>
            </view>
          </van-col>
        </van-col>
      </van-row>
      <van-row custom-class="line-item-row-gap">
        <van-col custom-class="line-item">
          <image class="line-item-image" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line3.png" />
            <lable class="line-item-desc-title">诗意梅州</lable>
            <label class="line-item-desc-info">体验禅意生活！</label>
            <view class="line-item-desc-footer">
              <image class="line-item-desc-like" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
              <label class="line-item-desc-like-count">10</label>
              <image class="line-item-desc-hotism" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/hot.png" />
              <label class="line-item-desc-hotism-count">1326</label>
            </view>
        </van-col>
        <van-col custom-class="line-item line-item-gap">
          <image class="line-item-image" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/line4.png" />
            <lable class="line-item-desc-title">梅州青山绿水</lable>
            <label class="line-item-desc-info">天然氧吧！</label>
            <view class="line-item-desc-footer">
              <image class="line-item-desc-like" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/like.png" />
              <label class="line-item-desc-like-count">8</label>
              <image class="line-item-desc-hotism" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/hot.png" />
              <label class="line-item-desc-hotism-count">1025</label>
            </view>
        </van-col>
      </van-row>
    </view>

    </view>
  </view>
</template>

<script>

export default {
  data() {
    return {}
  }
}
</script>

<style>
.container {
  width: 750rpx !important;
  height: 100%;
  text-align: center;
  display: block;
  align-items: center;
  justify-content: center;
}

.video-cover {
  width: 100%;
  height: 424rpx;
}

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
  height: 50rpx;
}

.desc-title-head-text {
  position: relative;
  top: -4rpx;
  font-size: 60rpx;
  font-weight: 800;
  margin-left: 4rpx;
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

.line-items {
  margin-top: 40rpx;
  text-align: left;
  margin-left: 30rpx;
  margin-right: 30rpx;
}

.line-items-head-text {
  text-align: left;
  font-size: 36rpx;
  font-weight: 600;
}

.line-items-filter {
  margin-top: 40rpx;
  margin-left: 50rpx;
  margin-right: 50rpx;
  padding-bottom: 40rpx;
}

.line-items-filter-condition {
  padding-right: 16rpx;
  border-right: solid 2rpx #F5F3F1;
}

.line-items-filter-text {
  margin-right: 30rpx;
  font-size: 30rpx;
  color: #838386;
  font-weight: 450;
}

.arrow-down {
  width: 20rpx;
  height: 10rpx;
  position: relative;
  top: -4rpx;
}

.line-items-filter-gap {
  margin-left: 20rpx;
}

.line-items-filter-selected {
  color: #000;
}

.line-item {
  width: 333rpx;
  border: solid 1rpx #F2F0ED;
  border-radius: 14rpx;
}

.line-item-gap {
  margin-left: 20rpx;
}

.line-item-row-gap {
  margin-top: 20rpx;
}

.line-item-image {
  width: 330rpx;
  height: 230rpx;
}

.line-item-desc-title {
  display: block !important;
  margin-left: 20rpx;
  font-size: 30rpx;
  font-weight: 500;
}

.line-item-desc-info {
  margin-left: 20rpx;
  font-size: 26rpx;
  color: #838386;
}

.line-item-desc-footer {
  margin-top: 35rpx;
  margin-left: 125rpx;
}

.line-item-desc-like {
  width: 30rpx;
  height: 30rpx;
}

.line-item-desc-like-count {
  font-size: 28rpx;
  position: relative;
  top: -4rpx;
  margin-left: 4rpx;
  font-weight: 500;
}

.line-item-desc-hotism {
  margin-left: 30rpx;
  width: 30rpx;
  height: 30rpx;
}

.line-item-desc-hotism-count {
  font-size: 28rpx;
  position: relative;
  top: -4rpx;
  margin-left: 4rpx;
  font-weight: 500;
}

.user-action {
  vertical-align:middle;
}

.card-thumb {
  width: 180px !important;
  height: 100px !important;
  border-radius: 15px;
}

.van-card__content {
  margin-left: 70px;
}
</style>
