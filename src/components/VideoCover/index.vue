<template>
  <!-- 封面模块 -->
  <view>
    <video 
    class="video-cover" 
    src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/video/cover.mp4" 
    objectFit="cover"
    poster="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/spot/cover.png" />
  </view>
</template>

<script>
export default {
  name: "VideoCover"
}
</script>

<style>
.video-cover {
  width: 100%;
  height: 424rpx;
}
</style>

