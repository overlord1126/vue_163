<template>
  <div style="height:100%;">
   <view-box id="scroll" ref="viewBox">
    <x-header 
    	slot="header"
   	style="width:100%;position:absolute;left:0;top:0;z-index:100;"
    	:title=opt.title
    	:left-options = opt
    	:right-options = "{showMore:true}"
    >
    	<!--This is the page title.-->
    </x-header>
    
    <tab>
      <tab-item width=2000 selected @on-item-click="go">已发货</tab-item>
      <tab-item @on-item-click="go">未发货</tab-item>
      <tab-item @on-item-click="go">全部订单</tab-item>
    </tab>
    
    <swiper id="sw"
    	:list="list"
    	auto
    	loop
    ></swiper>
    
    
    <marquee id="list"
    	:interval=500
    	:duration=300
    >
      <marquee-item v-for="i in 5" :key="i" @click.native="go()" class="align-middle">hello world {{i}}</marquee-item>
    </marquee>
    
    <div>
    	<panel :list="contentList" type="5"></panel>
    </div>
    
		<tabbar slot="bottom" 
		style="width:100%;position:absolute;left:0;bottm:0;z-index:100;">
		  <tabbar-item :show-dot="showDot">
		    <img slot="icon" src="">
		    <span slot="label">游戏</span>
		  </tabbar-item>
		  <tabbar-item selected link="/component/demo">
		    <img slot="icon" src="">
		    <span slot="label">科技</span>
		  </tabbar-item>
		  <tabbar-item badge="2">
		    <img slot="icon" src="">
		    <span slot="label">前端</span>
		  </tabbar-item>
		</tabbar>
    
   </view-box>
 </div>
</template>

<script>

import { 
	XHeader ,
	Swiper ,
	Tabbar, 
	TabbarItem, 
	Tab, 
	TabItem,
	Marquee, 
	MarqueeItem, 
	Panel,
	ViewBox 
} from 'vux'

export default {
	data(){
		return {
			opt:{
				title:"标题页面",
				showBack:true,
				backText:"Back"
			},
			a:"red",
			showDot:true,
			list:[{
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/1.jpg',
			  title: '送你一朵花'
			}, {
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/2.jpg',
			  title: '送你一辆车'
			},{
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/3.jpg',
			  title: '送你一次旅行'
			},{
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/1.jpg',
			  title: '送你一朵花'
			}, {
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/2.jpg',
			  title: '送你一辆车'
			},{
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/3.jpg',
			  title: '送你一次旅行'
			}, {
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/1.jpg',
			  title: '送你一朵花'
			}, {
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/2.jpg',
			  title: '送你一辆车'
			},{
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/3.jpg',
			  title: '送你一次旅行'
			}],
			contentList:[
				{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				},{
					src: 'http://placeholder.qiniudn.com/60x60/3cc51f/ffffff',
	        title: '标题一',
	        desc: '由各种物质组成的巨型球状天体，叫做星球。星球有一定的形状，有自己的运行轨道。'
				}
			]
		}
	},
  components: {
    XHeader,
    Swiper,
    Tabbar,
    TabbarItem,
    Tab, 
    TabItem,
    Marquee, 
    MarqueeItem,
    Panel,
    ViewBox 
  },
  methods: {
  	go:function(){
//		alert(1)
  	}
  }
}
</script>
<style scoped>
	#scroll {
		padding-top: 44px;
		box-sizing: border-box;
	}
	#list{
		background-color: whitesmoke;
	}
	#list li{
		line-height: 40px;
		text-align: left;
		text-indent: 20px;
	}
	#sw{
		text-align: left;
	}
</style>