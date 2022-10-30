<template>
  <view class="content">
    <image class="logo" src="/static/logo.png"></image>
    <view class="text-area">
      <text class="title">{{ title }}</text>
      <uni-badge text="厚度刷">啊哈哈哈</uni-badge>
    </view>
    <view>
      <uni-calendar
        :insert="true"
        :lunar="true"
        :start-date="'2019-3-2'"
        :end-date="'2019-5-20'"
      />
    </view>
  </view>
</template>

<script>
import uniBadge from '@dcloudio/uni-ui/lib/uni-badge/uni-badge'
import uniCalendar from '@dcloudio/uni-ui/lib/uni-calendar/uni-calendar'
import {add} from "mathjs"
export default {
  data() {
    return {
      title: 'Hello',
    }
  },
  components: {
    uniBadge,
    uniCalendar
  },
  onLoad() {
    console.log(add(0.1, 0.2))
  },
  methods: {},
}
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin-top: 200rpx;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 50rpx;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
