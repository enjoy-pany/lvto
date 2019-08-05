<template>
  <div>
    <div class="head-nav">
      <div class="iconWrap navLeft">
        <i class="iconfont icon-category"></i>
      </div>
      <div class="iconWrap navCenter">
        <i class="iconfont icon-calendar"></i>
      </div>
      <div class="iconWrap navRight">
        <i class="iconfont icon-edit"></i>
      </div>
    </div>
    <div class="mainCon">
      <div class="cus-cardList" v-for="item in list" :key="item.id" @click="goDetail($event)">
        <div class="cusDateBar" v-bind:class="{barHeader:item.isHeader}">
          <div class="date-icon">
            <em v-if="item.isHeader"></em>
          </div>
          <div class="date-num" v-if="item.isHeader">{{item.date}}</div>
        </div>
        <div class="cus-card" v-bind:style="{backgroundImage: 'url('+item.coverImg+')'}">
          <div class="card-text" :id="item.id">
            <div class="card-text-title">{{item.title}}</div>
            <div class="card-text-content">{{item.content}}</div>
          </div>
          <div class="card-action">
            <i class="iconfont icon-map"></i>
            <div class="postion">{{item.position}}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: true,
      list: [
        {
          id: 1,
          coverImg: 'https://enjoy-pany.github.io/view/assets/010.jpg',
          title: '雾灵山游记',
          content:
            '山泉人家，源自山泉。地处雾灵湖畔、雾灵山中，清新经营逾十年，只为分享给你清新的空气，纯净的泉水，秀丽的山色美景。',
          position: '北京市密云雾灵西峰风景区',
          date: '2017.06.08',
          isHeader: true
        },
        {
          id: 2,
          coverImg: 'https://enjoy-pany.github.io/view/assets/011.jpg',
          title: '十渡之旅',
          content:
            '十渡风景区位于北京市房山区西南，是中国北方唯一一处大规模喀斯特岩溶地貌。房山世界地质公园共有八个园区，其中十渡为八个园区的核心园区——十渡园区。',
          position: '北京市房山区西南十渡风景区',
          date: '2017.05.10',
          isHeader: false
        }
      ]
    }
  },
  methods: {
    goDetail (eve) {
      let _id = eve.target.id
      if (_id) {
        this.$router.push({ path: '/detail?id=' + _id })
      }
    }
  },
  mounted () {
    // this.$http.get("../../../static/mock/trace.json").then(
    //   res => {
    //     this.list = res.data;
    //   },
    //   res => {
    //     console.log(res);
    //   }
    // );
  }
}
</script>

<style scoped lang="less">
.head-nav {
  width: 100%;
  height: 88rpx;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  box-sizing: border-box;
  background: #2e9e64;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 9;
  .iconWrap  {
    padding: 0 30rpx;
    i {
      font-size: 38rpx;
      color: #fff;
    }
  }
}
.mainCon {
  width: 100%;
  height: 100%;
  margin-top: 88rpx;
  padding: 0 10rpx;
  box-sizing: border-box;
}
.cus-cardList {
  .cusDateBar {
    width: 100%;
    height: 20rpx;
    position: relative;
    .date-icon {
      display: inline-block;
      width: 5rpx;
      height: 100%;
      background: #eee;
      position: absolute;
      left: 2%;
      top: 0;
    }
    .date-icon em {
      display: inline-block;
      width: 10rpx;
      height: 10rpx;
      border-radius: 50rpx;
      background: #009688;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%,-50%);
    }
    .date-num {
      display: inline-block;
      font-size: 26rpx;
      font-weight: 600;
      line-height: 60rpx;
      position: absolute;
      left: 5%;
      top: 0;
    }
  }
  .barHeader {
    height: 50rpx;
  }
  .cus-card {
    width: 100%;
    height: 300rpx;
    display: flex;
    justify-content: center;
    align-items: center;
    background-size: 100%;
    position: relative;
    overflow: hidden;
    .card-text {
      width: 100%;
      height: 300rpx;
      display: flex;
      /* justify-content: center;*/
      align-items: center;
      flex-direction: column;
      background: rgba(0, 0, 0, 0.4);
      color: #fff;
      .card-text-title {
        font-size: 30rpx;
        margin-top: 5%;
      }
      .card-text-content {
        width: 50%;
        height: 40%;
        display: inline-block;
        font-size: 20rpx;
        margin-top: 50rpx;
        overflow: hidden;
      }
    }
    .card-action {
      position: absolute;
      color: #fff;
      bottom: 5%;
      right: 5%;
      font-size: 14rpx;
      i {
        display: inline-block;
        font-size: 20rpx;
        color: #fff;
      }
      .postion {
        height: 100%;
        display: inline-block;
        margin-left: 5rpx;
      }
    }
  }
}




</style>