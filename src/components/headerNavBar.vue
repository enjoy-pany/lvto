<template>
  <div class="header-nav">
    <ul class="nav-list">
      <li 
        v-for="(item,index) in navList"
        :key="index"
        :class="{active: nowTab === index}"
        @click="changeTabIndex(index)">{{item.label}}</li>
    </ul>
    <i class="icon iconfont icon-information" @click="showDialog"></i>
  </div>
</template>
<script>
export default {
  data() {
    return {
      nowTab: 0,
      navList: [
        {
          label: '最新'
        },
        {
          label: '最热'
        },
        {
          label: '我的'
        }
      ]
    }
  },
  methods: {
    changeTabIndex(index) {
      this.nowTab = index
    }
  }
}
</script>
<style lang="less" scoped>
.header-nav {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9;
  width: 100%;
  height: 88rpx;
  background: #2e9e64;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  .nav-list {
    width: 320rpx;
    height: 60rpx;
    background: #fff;
    border-radius: 10rpx;
    border: 2rpx #fff solid;
    display: flex;
    align-items: center;
    justify-content: space-between;
    overflow: hidden;
    li {
      width: 33%;
      height: 100%;
      color: #fff;
      font-size: 20rpx;
      text-align: center;
      line-height: 60rpx;
      background: #2e9e64;
    }
    .active {
      color: #2e9e64;
      background: #fff;
    }
  }
  .icon{
    font-size: .38rem;
    color: #fff;
    position: absolute;
    top: 30%;
    right: 5%;
  }
}
</style>
