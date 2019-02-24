<template>
<van-dialog
  use-slot
  title="更多精彩敬请期待"
  :show="get_comingsoon_dialog_show"
  @confirm="onConfirm"
>

<van-row custom-class="dialog-image-layout">
  <image class="dialog-image" src="https://7065-perfect9photos-b0f95d-1258496539.tcb.qcloud.la/static/image/caicai.png" />
</van-row>


<van-row custom-class="dialog-text-title">
  <label>九图计划</label>
</van-row>
<van-row custom-class='dialog-declare-text'>
  <label class="dialog-declare-text">智慧全域旅游一站式解决方案</label>
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

.dialog-text-title {
  text-align: center;
  margin-top: 30rpx;
}

.dialog-declare-text {
  text-align: center;
  color: #838386;
  font-size: 26rpx;
  margin-top: 10rpx;
  margin-bottom: 40rpx;
}

.dialog-image-layout {
  text-align: center;
}

.dialog-image {
  width: 160rpx;
  height: 208rpx;
  margin-top: 50rpx;
}
</style>
