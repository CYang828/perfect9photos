<template>
<!-- 封面模块 -->
<view>
  <!-- <map class="line-navagation-map" subkey="U5FBZ-YMM6G-5OJQY-IORMX-YKISV-TCB4Z"
  longitude="116.128679"
  latitude="24.294506"
  :markers="markers"
  scale=14 />
-->
  <image mode="scaleToFill" class="line-navagation-map" src="https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/spot/map-conver.jpg" />
  </view> 

</template>

<script>
export default {
  name: "MapCover",
  props: ['markers']
}
</script>

<style>
.line-navagation-map {
  width: 100%;
  height: 854rpx;
}
</style>
