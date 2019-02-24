<template>
<view>
  <view>
    <image @click="comingsoon" class="fake-image" mode="widthFix" src="https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/page2-1.png" />
    <a href="/pages/line/main" class="fake-images-gap">
      <image class="fake-image" mode="widthFix" src="https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/page2-2.png" />
    </a>
  </view>
  <coming-soon-dialog />
</view>
</template>

<script>
import {mapMutations} from 'vuex'
import {SET_COMINGSOON_DIALOG_SHOW} from '@/store/mutation-types'
import ComingSoonDialog from '@/components/ComingSoonDialog/index.vue'

export default {
  data () {
    return {}
  },
  methods: {
    ...mapMutations([
      SET_COMINGSOON_DIALOG_SHOW
    ]),
    comingsoon () {
      console.log('hello')
      this[SET_COMINGSOON_DIALOG_SHOW](true)
    }
  },
  components: {
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

.fake-image {
  width: 750rpx;
}

.fake-images-gap {
  margin-top: -15rpx;
}
</style>
