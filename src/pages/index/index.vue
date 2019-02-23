<template>
  <view class="container">
    <index-cover />
    <view class="card-border">
      <recommand-location />
      <user-comment />
    </view>
    <coming-soon-dialog />
  </view>
</template>

<script>
import IndexCover from '@/components/IndexCover/index.vue'
import RecommandLocation from '@/components/RecommandLocation/index.vue'
import UserComment from '@/components/UserComment/index.vue'
import ComingSoonDialog from '@/components/ComingSoonDialog/index.vue'

export default {
  data () {
    return {}
  },
  components: {
    IndexCover,
    RecommandLocation,
    UserComment,
    ComingSoonDialog
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
  z-index: 99;
  background-color: #fff;
}

</style>

