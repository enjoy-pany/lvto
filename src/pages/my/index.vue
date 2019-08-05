<template>
  <div class="mineCon">
    <div class="userInfo">
      <div class="mu-avatar">
        <img :src="userInfo.avatar" />
      </div>
      <div class="userName">{{userInfo.name}}</div>
      <div class="userDesc">{{userInfo.desc}}</div>
    </div>
    <div class="seleList">
      <ul class="seleListMar mu-list">
        <li class="mu-list-item">
          <i class="iconfont icon-form"></i>
          <p>修改资料</p>
          <i class="iconfont icon-more"></i>
        </li>
        <li class="mu-list-item">
          <i class="iconfont icon-jewelry"></i>
          <p>成为VIP</p>
          <i class="iconfont icon-more"></i>
        </li>
      </ul>
      <ul class="seleListMar mu-list">
        <li class="mu-list-item">
          <i class="iconfont icon-comments"></i>
          <p>系统通知</p>
          <i class="iconfont icon-more"></i>
        </li>
      </ul>
      <ul class="seleListMar mu-list">
        <li class="mu-list-item">
          <i class="iconfont icon-good"></i>
          <p>好评鼓励</p>
          <i class="iconfont icon-more"></i>
        </li>
        <li class="mu-list-item">
          <i class="iconfont icon-viewgallery"></i>
          <p>更多功能</p>
          <i class="iconfont icon-more"></i>
        </li>
        <li class="mu-list-item">
          <i class="iconfont icon-set"></i>
          <p>设置</p>
          <i class="iconfont icon-more"></i>
        </li>
        <li class="mu-list-item">
          <i class="iconfont icon-gifts"></i>
          <p>分享有礼</p>
          <i class="iconfont icon-more"></i>
        </li>
      </ul>
    </div>
    <div class="exitBtn">
      <button class="btn" type="button">退出登录</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userInfo: {
        name: 'Pany',
        avatar: require('../../../static/images/defaultAva.jpg'),
        desc: 'wish sunshine everyday'
      }
    }
  }
}
</script>

<style scoped lang="less">
.mineCon {
  width: 100%;
  height: 100%;
  background: #eff4f7;
  /*margin-bottom: 1rem; */
}
.userInfo {
  width: 100%;
  height: 350rpx;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background: #00bcd4 url("https://enjoy-pany.github.io/view/assets/defaultBg.jpg") no-repeat center;
  background-size: 100% 100%;
  margin-bottom: 30rpx;
  color: #fff;
  font-size: 48rpx;
  .mu-avatar {
    width: 150rpx;
    height: 150rpx;
    img {
      width: 100%;
      height: 100%;
    }
  }
  .userName {
    font-size: 34rpx;
    margin-top: 10rpx;
  }
  .userDesc {
    font-size: 28rpx;
    margin-top: 10rpx;
  }
}
.seleList {
  .seleListMar {
    margin-bottom: 20rpx;
  }
  .mu-list {
    width: 100%;
    background: #fff;
    font-size: 48rpx;
    li {
      width: 100%;
      height: 90rpx;
      display: flex;
      justify-content: center;
      align-content: center;
      i {
        font-size: 40rpx;
        color: #31a067;
        line-height: 90rpx;
      }
      p {
        width: 80%;
        height: 100%;
        font-size: 30rpx;
        line-height: 90rpx;
        text-indent: 2em;
      }
    }
  }
} 
.exitBtn {
  width: 100%;
  height: 150rpx;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #eff4f7;
  .btn {
    width: 400rpx;
    height: 60rpx;
    border: none;
    line-height: 60rpx;
    background: #ee7a7a;
    font-size: 30rpx;
    color: #fff;
    border-radius: 10rpx;
  }
}
</style>
