<template>
  <!-- 封面模块 -->
    <view>
      <image class="cover-image" mode="scaleToFill" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/cover.png" />
      <view class="location">
        <van-cell custom-class="location-cell" v-bind:border="false" center>
          <view slot="title">
            <label class="location-name">北京</label>
            <image class="triangle-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/triangle.png" />
          </view>
        </van-cell>
        <van-cell custom-class="location-cell" v-bind:border="false" center>
          <view slot="title" class="align">
            <image class="sun-icon" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/sun.png" />
            <label class="temperature">25°</label>
          </view>
        </van-cell>
      </view>
      <van-search custom-class="search" background="#fff" placeholder-class="search-placeholder" maxlength="50" placeholder="请输入目的地" />
    </view>
</template>

<script>
export default {
  name: "IndexCover"
}
</script>

<style>
.cover-image {
  width: 100%;
  height: 804rpx;
  z-index: 98;
}
.align {
  display: flex;
}

.location {
  position: absolute;  
  top: 326rpx;
  opacity: 0.95;
  z-index: 99;
  margin-left: 33%;
}

.location-cell {
  padding: 6rpx 30rpx !important;
  background-color: transparent !important;
}

.location-name {
  padding-left: 40rpx;
  font-size: 52rpx;
  font-weight: 600;
  color: #fff;
}

.triangle-icon {
  width: 20rpx;
  height: 16rpx;
  margin-left: 10rpx;
  margin-bottom: 10rpx;
  font-size: 20rpx !important;
  color: #fff;
}

.sun-icon {
  width: 50rpx;
  height: 50rpx;
  opacity: 95%;
  padding-left: 40rpx;
}

.temperature {
  color: #fff;
  font-size: 30rpx;
  font-weight: 500;
  margin-left: 10rpx; 
  margin-top: 2rpx;
}

.search {
  position: absolute;  
  top: 636rpx;  
  left: 5%;
  width: 90%;
  height: 84rpx;
  opacity: 0.95;
  z-index: 99;
  border-radius:60rpx;
}

.van-search__field {
  margin-left: 30%;
}
</style>

