<template>
<van-dialog
  use-slot
  title="更多精彩敬请期待"
  :show="get_comingsoon_dialog_show"
  @confirm="onConfirm"
>
<van-row>
  <van-col custom-class="dialog-text">
    <van-row>
      <label>九图计划</label>
    </van-row>
    <van-row>
      <label class="dialog-declare-text">智慧全域旅游一站式解决方案</label>
    </van-row>
  </van-col>
  <van-col>
    <image class="dialog-image" src="cloud://perfect9photos-b0f95d.7065-perfect9photos-b0f95d/static/image/index/caicai.png" />
  </van-col>
</van-row>
</van-dialog>
</template>

<script>
import { mapState, mapMutations } from 'vuex'
import {SET_COMINGSOON_DIALOG_SHOW} from '@/store/mutation-types'

export default {
  name: 'ComingSoonDialog',
  data() {
    return {}
  },
  computed: {
    ...mapState([
      'comingsoon_dialog_show'
    ]),
    get_comingsoon_dialog_show () {
      return this.$store.state.comingsoon_dialog_show
    }
  },
  methods: {
    ...mapMutations([
      SET_COMINGSOON_DIALOG_SHOW
    ]),
    onConfirm () {
      this[SET_COMINGSOON_DIALOG_SHOW](false)
    }
  }
};
</script>

<style>
.dialog-text{
  text-align: left;
  margin-left: 80rpx;
  margin-top: 100rpx;
}

.dialog-declare-text {
  color: #838386;
  font-size: 22rpx;
  margin-top: 30rpx;
}

.dialog-image {
  width: 104rpx;
  height: 150rpx;
  margin-top: 60rpx;
  margin-left: 100rpx;
}
</style>
