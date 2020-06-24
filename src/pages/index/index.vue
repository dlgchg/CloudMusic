<template>
  <view class="content">
    <scroll-view scroll-y="true">
      <swiper
        class="swiper"
        indicator-dots="true"
        autoplay="true"
        indicator-color="#bdbdbd"
        indicator-active-color="#ffffff"
      >
        <swiper-item v-for="item in swiperData" :key="item.src">
          <view class="swiper-item uni-bg-red">
            <image
              class="swiper-item-image"
              :src="item.src"
              mode="aspectFill"
            />
          </view>
        </swiper-item>
      </swiper>
      <view class="bar-layout">
        <view class="bar-item">
          <image src="../../static/image/singer_icon.png" />
          <text>歌手</text>
        </view>
        <view class="bar-item">
          <image src="../../static/image/ranking_icon.png" />
          <text>排行</text>
        </view>
        <view class="bar-item">
          <image src="../../static/image/category_icon.png" />
          <text>分类</text>
        </view>
        <view class="bar-item">
          <image src="../../static/image/station_icon.png" />
          <text>电台</text>
        </view>
        <view class="bar-item">
          <image src="../../static/image/live_icon.png" />
          <text>直播</text>
        </view>
      </view>
      <view class="layout-flex-row">
        <view class="card">
          <image
            src="http://p4.music.126.net/kzdfn8XZnw99wmj_vl4dfg==/109951163200239897.jpg"
            mode="aspectFill"
          />
          <view class="left">
            <text class="left-title">新歌新碟</text>
            <text class="left-desc">周杰伦新歌快递</text>
          </view>
        </view>
        <view class="card">
          <image
            src="http://p4.music.126.net/kzdfn8XZnw99wmj_vl4dfg==/109951163200239897.jpg"
            mode="aspectFill"
          />
          <view class="left">
            <text class="left-title">新歌新碟.票务</text>
            <text class="left-desc">周杰伦新歌快递</text>
          </view>
        </view>
      </view>
      <scroll-view scroll-x="true">
        <view class="flex-grid">
          <view>#杨超越崩溃式毕业告白</view>
          <view>#G-Eazy全新抒情新歌MV</view>
          <view>#杨超越崩溃式毕业告白</view>
          <view>#星爷版无价之姐6</view>
          <view>##seventeen回归初舞台!</view>
          <view>#DER-妖精帝國(ようせい</view>
        </view>
      </scroll-view>

      <view class="header">
        <view class="title">超热歌单</view>
        <view class="more">更多</view>
      </view>
      <scroll-view scroll-x="true">
        <view class="flex-grid-hot">
          <view class="grid">
            <view class="content" v-for="item in hotData" :key="item.src">
              <view class="content-card">
                <image class="icon" :src="item.src" mode="aspectFill" />
                <view class="num">
                  <image src="../../static/image/erji.png" />
                  <text>{{ item.playnum }}万</text>
                </view>
                <image class="play" src="../../static/image/play_white.png" />
              </view>
              <view class="title">{{ item.title }}</view>
            </view>
          </view>
        </view>
      </scroll-view>
	  <view class="header">
        <view class="title">大家都在听</view>
        <view class="more">更多</view>
      </view>
	  <scroll-view scroll-x="true">
        <view class="flex-grid-all">
         <view class="content" v-for="item in alllesten" :key="item.src">
              <image :src="item.src" mode="aspectFill" />
              <view class="right">
				  <view class="title">{{ item.title }}</view>
				  <view class="desc">
					  {{ item.desc }}
					  <text class="hotplay" v-if="item.hot">今日热播<text/>

				  </view>
			  </view>
			   <image class="play" src="../../static/image/play_gray.png" />
            </view>
        </view>
      </scroll-view>
    </scroll-view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: "音乐馆",
      swiperData: [
        {
          src:
            "http://p4.music.126.net/kzdfn8XZnw99wmj_vl4dfg==/109951163200239897.jpg",
        },
        {
          src:
            "http://static.statickksmg.com/image/2012/12/05/fe011ce9517cc65750227ce3923c7982.jpg",
        },
        {
          src:
            "http://n.sinaimg.cn/translate/368/w700h468/20181012/LGw0-hktxqai6658212.jpg",
		},
		{
			src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
		},
		{
			src: "http://gb.cri.cn/mmsource/images/2007/11/30/em071129044.jpg",
		},
		{
			src: "https://tse4-mm.cn.bing.net/th/id/OIP.1SCLEwE1jswuA3sstI7emAHaHa?pid=Api&rs=1",
		},
		{
			src: "https://y.gtimg.cn/music/photo_new/T002R300x300M000001Zrk6t0urxvG.jpg?max_age=2592000",
		},
		{
			src: "http://c4.haibao.cn/img/600_0_100_0/liqb7DBFHlH9M/piccommon/1178/11782/liqb7DBFHlH9M.jpg",
		},
		{
			src: "https://y.gtimg.cn/music/photo_new/T002R300x300M000003yeNV10Tzs9v.jpg?max_age=2592000",
		},
		{
			src:  "http://img1.cache.netease.com/ent/2014/7/15/201407150923194d705_550.jpg",
		},
      ],
      hotData: [
        {
          src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
          playnum: 1234,
          title: "周杰伦的睡前故事",
        },
        {
          src: "http://gb.cri.cn/mmsource/images/2007/11/30/em071129044.jpg",
          playnum: 222,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "https://tse4-mm.cn.bing.net/th/id/OIP.1SCLEwE1jswuA3sstI7emAHaHa?pid=Api&rs=1",
          playnum: 235,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "https://y.gtimg.cn/music/photo_new/T002R300x300M000001Zrk6t0urxvG.jpg?max_age=2592000",
          playnum: 456,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "http://ent.cctv.com/20080109/images/1199842596133_8341314307139175291.jpg",
          playnum: 2466,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "http://i0.sinaimg.cn/ent/y/d/2009-04-07/U1978P28T3D2459150F359DT20090407120634.jpg",
          playnum: 109,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "https://tse3-mm.cn.bing.net/th/id/OIP.555iYiOihPPJPiUR7EpJbQHaHa?pid=Api&rs=1",
          playnum: 555,
          title: "周杰伦的睡前故事",
        },
        {
          src: "https://img3.doubanio.com/img/biz/poster-1445262720.jpg",
          playnum: 109,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "https://img.zcool.cn/community/01f709587ddb0ba801219c777fa3a4.jpg@1280w_1l_2o_100sh.jpg",
          playnum: 1002,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "http://c4.haibao.cn/img/600_0_100_0/liqb7DBFHlH9M/piccommon/1178/11782/liqb7DBFHlH9M.jpg",
          playnum: 1509,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "http://img1.cache.netease.com/ent/2014/7/15/201407150923194d705_550.jpg",
          playnum: 890,
          title: "周杰伦的睡前故事",
        },
        {
          src:
            "https://y.gtimg.cn/music/photo_new/T002R300x300M000003yeNV10Tzs9v.jpg?max_age=2592000",
          playnum: 689,
          title: "周杰伦的睡前故事",
        },
	  ],
	  alllesten: [
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: true
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: false
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: false
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: false
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: true
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: false
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: false
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: true
		  },
		  {
			  src: "http://n.sinaimg.cn/transform/20151030/xaxQ-fxkhcfq0982007.jpg",
			  title: "后来遇见他",
			  desc: "胡66.另一个我",
			  hot: false
		  }
		  
	  ]
    };
  },
  onLoad() {},
  methods: {},
};
</script>

<style>
.content {
  text-align: center;
  height: 400upx;
}

.logo {
  height: 200upx;
  width: 200upx;
  margin-top: 200upx;
}

.title {
  font-size: 36upx;
  color: #8f8f94;
}
.swiper {
  height: 150px;
}
.swiper-item {
  height: 150px;
}
.swiper-item-image {
  border-radius: 8px;
  width: 92%;
  height: 150px;
}
.bar-layout {
  display: flex;
  justify-content: space-evenly;
  padding: 10px 0;
}
.bar-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;
  height: 70px;
}
.bar-item image {
  width: 25px;
  height: 25px;
}
.bar-item text {
  font-weight: 200;
}
.layout-flex-row {
  display: flex;
  flex-direction: row;
  padding: 10px;
  justify-content: space-evenly;
}
.card {
  background-color: #f2f2f2;
  padding: 10px;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  border-radius: 5px;
}
.card image {
  width: 50px;
  height: 50px;
  border-radius: 5px;
}
.card .left {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  margin-left: 10px;
  align-items: flex-start;
}

.card .left .left-title {
  font-size: 14px;
}
.card .left .left-desc {
  font-size: 12px;
  color: #888789;
}
.flex-grid,
.flex-grid-hot,
.flex-grid-all{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  padding: 10px;
  white-space: nowrap;
  width: 150%;
}
.flex-grid view {
  font-size: 14px;
  font-weight: 300;
  padding: 5px 10px;
  background-color: #f2f2f2;
  border-radius: 50px;
  margin-top: 10px;
  margin-left: 10px;
}
.flex-grid-hot {
  flex-direction: column;
  padding: 10px 10px 0 10px;
  width: 200%;
}
.header {
  display: flex;
  justify-content: space-between;
  padding: 5px 20px;
  align-items: center;
}
.header .title {
  font-size: 22px;
  font-weight: 500;
  color: #000000;
}
.header .more {
  font-size: 14px;
  color: gray;
}
.flex-grid-hot .grid {
  display: flex;
  flex-wrap: wrap;
}
.flex-grid-hot .grid .content {
  display: flex;
  flex-direction: column;
  margin-left: 10px;
  height: 150px;
}
.flex-grid-hot .grid .content .title {
  width: 100px;
  font-weight: 200;
  font-size: 13px;
  word-break: break-all;
  white-space: pre-wrap;
  color: #000000;
  text-align: left;
}
.flex-grid-hot .grid .content .content-card {
  position: relative;
  width: 110px;
  display: flex;
  align-items: center;
  height: 110px;
}
.flex-grid-hot .grid .content .content-card .icon {
  width: 110px;
  height: 110px;
  border-radius: 10px;
}
.flex-grid-hot .grid .content .content-card .num {
  position: absolute;
  bottom: 10px;
  left: 10px;
  color: #ffffff;
}
.flex-grid-hot .grid .content .content-card image {
  width: 15px;
  height: 15px;
}
.flex-grid-hot .grid .content .content-card text {
  font-size: 10px;
}
.flex-grid-hot .grid .content .content-card .play {
  position: absolute;
  bottom: 10px;
  right: 10px;
  width: 20px;
  height: 20px;
}

.flex-grid-all {
  padding: 10px 10px 0 10px;
  width: 280vw;
}
.flex-grid-all .content{
	width: 90vw;
	height: 50px;
	display: flex;
	flex-direction: row;
	margin-left: 10px;
	margin-top: 10px;
}
.flex-grid-all .content image {
	width: 50px;
	height: 50px;
	border-radius: 5px;
}
.flex-grid-all .content .right {
	display: flex;
	flex-direction: column;
	align-items: flex-start;
	margin-left: 10px;
	flex: 1;
}
.flex-grid-all .content .right .title {
	font-size: 14px;
	margin-bottom: 5px;
	margin-top: 5px;
	color: #000;
}
.flex-grid-all .content .right .desc {
	font-size: 11px;
	color: #888789;
}
.flex-grid-all .content .right .desc .hotplay{
	background-color: #21D49D;
	padding: 1px 3px;
	border-radius: 2px;
	color: white;
	font-size: 8px;
	margin-left: 10px;
}
.flex-grid-all .content .play {
	width: 22px;
	height: 22px;
	align-self: center;
	margin-right: 10px;
}
</style>
