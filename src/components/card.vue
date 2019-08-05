<template>
  <div class="mainCon">
    <div class="card" v-for="(item, index) in list" :key="index">
      <div class="card-header">
        <div class="avatar">
          <img :src="item.avatar" alt />
        </div>
        <div class="userInfo">
          <div class="header-title">{{item.author}}</div>
          <div class="header-sub-title">{{item.desc}}</div>
        </div>
      </div>
      <div class="card-media">
        <img :src="item.image"  mode="widthFix" />
        <div class="card-img-title">
          <div class="img-title">{{item.imageTitle}}</div>
          <div class="img-sub-title">{{item.imageSubTitle}}</div>
        </div>
      </div>
      <div class="card-text">{{item.content}}</div>
      <div class="card-actions">
        <span class="time">4小时前</span>
        <i id="favorite" class="iconfont icon-good"></i>
        <i id="good" class="iconfont icon-favorite"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [
        {
          avatar: 'https://enjoy-pany.github.io/view/assets/defaultAva.jpg',
          author: 'Myron',
          desc: 'sub title',
          image: 'https://enjoy-pany.github.io/view/assets/008.jpg',
          imageTitle: 'Breakfast',
          imageSubTitle: 'image sub title',
          content:
            '散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光, 找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！',
          featured: true
        },
        {
          avatar: 'https://enjoy-pany.github.io/view/assets/defaultAva.jpg',
          author: 'Myron',
          desc: 'sub title',
          image: 'https://enjoy-pany.github.io/view/assets/001.jpg',
          imageTitle: 'Breakfast',
          imageSubTitle: 'image sub title',
          content:
            '散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光, 找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！',
          featured: true
        },
        {
          avatar: 'https://enjoy-pany.github.io/view/assets/defaultAva.jpg',
          author: 'Myron',
          desc: 'sub title',
          image: 'https://enjoy-pany.github.io/view/assets/002.jpg',
          imageTitle: 'Breakfast',
          imageSubTitle: 'image sub title',
          content:
            '散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光, 找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！',
          featured: true
        },
        {
          avatar: 'https://enjoy-pany.github.io/view/assets/defaultAva.jpg',
          author: 'Myron',
          desc: 'sub title',
          image: 'https://enjoy-pany.github.io/view/assets/003.jpg',
          imageTitle: 'Breakfast',
          imageSubTitle: 'image sub title',
          content:
            '散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光, 找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！',
          featured: true
        },
        {
          avatar: 'https://enjoy-pany.github.io/view/assets/defaultAva.jpg',
          author: 'Myron',
          desc: 'sub title',
          image: 'https://enjoy-pany.github.io/view/assets/004.jpg',
          imageTitle: 'Breakfast',
          imageSubTitle: 'image sub title',
          content:
            '散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光, 找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！',
          featured: true
        },
        {
          avatar: 'https://enjoy-pany.github.io/view/assets/defaultAva.jpg',
          author: 'Myron',
          desc: 'sub title',
          image: 'https://enjoy-pany.github.io/view/assets/005.jpg',
          imageTitle: 'Breakfast',
          imageSubTitle: 'image sub title',
          content:
            '散落在指尖的阳光，我试着轻轻抓住光影的踪迹，它却在眉宇间投下一片淡淡的阴影。调皮的阳光掀动了四月的心帘，温暖如约的歌声渐起。似乎在诉说着，我也可以在漆黑的角落里，找到阴影背后的阳光, 找到阳光与阴影奏出和谐的旋律。我要用一颗敏感赤诚的心迎接每一缕滑过指尖的阳光！',
          featured: true
        }
      ]
    }
  },
  methods: {},
  mounted() {}
}
</script>

<style lang="less" scoped>
.mainCon {
  width: 100%;
  padding: 0 10rpx;
  margin-top: 88rpx;
  margin-bottom: 10rpx;
  box-sizing: border-box;
  .card {
    width: 100%;
    background-color: #fff;
    border-radius: 2rpx;
    box-shadow: 0 1rpx 6rpx rgba(0, 0, 0, 0.117647),
      0 1rpx 4rpx rgba(0, 0, 0, 0.117647);
    margin: 10rpx 0;
    .card-header {
      width: 100%;
      height: 100rpx;
      display: flex;
      align-items: center;
      .avatar {
        width: 60rpx;
        height: 60rpx;
        border-radius: 30rpx;
        margin: 0 20rpx;
        img {
          display: block;
          width: 100%;
          height: 100%;
        }
      }
    }
    .userInfo {
      .header-title {
        font-size: 24rpx;
      }
      .header-sub-title {
        font-size: 20rpx;
        color: rgba(0, 0, 0, 0.57);
      }
    }
    .card-media {
      width: 100%;
      position: relative;
      left: 0;
      top: 0;
      img {
        display: block;
        width: 100%;
        height: 100%;
      }
      .card-img-title {
        width: 100%;
        height: 100rpx;
        position: absolute;
        left: 0;
        bottom: 0;
        background: rgba(0, 0, 0, 0.5);
        padding: 20rpx;
        box-sizing: border-box;
        .img-title {
          color: rgba(255, 255, 255, 0.9);
          font-size: 28rpx;
        }
        .img-sub-title {
          color: rgba(255, 255, 255, 0.5);
          font-size: 24rpx;
        }
      }
    }
    .card-text {
      width: 100%;
      font-size: 20rpx;
      padding: 30rpx 20rpx;
      box-sizing: border-box;
    }
    .card-actions {
      width: 100%;
      height: 50rpx;
      font-size: 20rpx;
      padding: 0 20rpx;
      box-sizing: border-box;
      display: flex;
      justify-content: space-around;
      align-items: center;
      i {
        font-size: 24rpx;
      }
      .time {
        color: rgba(0, 0, 0, 0.7);
      }
    }
  }
}
</style>