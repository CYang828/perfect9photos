<template>
  <view class="container">
    <index-cover />
    <view class="card-border">
      <recommand-location />
      <user-comment />
    </view>
  </view>
</template>

<script>
import IndexCover from '@/components/IndexCover/index.vue'
import RecommandLocation from '@/components/RecommandLocation/index.vue'
import UserComment from '@/components/UserComment/index.vue'

export default {
  data () {
    return {}
  },
  components: {
    IndexCover,
    RecommandLocation,
    UserComment
  }
}
</script>

<style>
.container {
  height: 100%;
  text-align: center;
  display: block;
  align-items: center;
  justify-content: center;
}

.card-border {
  position: absolute;
  display: block;
  border-radius: 20rpx;
  top: 790rpx;
  z-index: 999;
  background-color: #fff;
}

</style>
