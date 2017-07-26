<template>
  <div >
    <x-header 
    	:title=opt.title
    	:left-options = opt
    	:right-options = "{showMore:true}"
    >
    	<!--This is the page title.-->
    </x-header>
    <swiper 
    	:list="list"
    	auto
    	loop
    
    ></swiper>
  </div>
</template>

<script>

import { XHeader ,Swiper  } from 'vux'

export default {
	data(){
		return {
			opt:{
				title:"标题页面",
				showBack:true,
				backText:"Back"
			},
			list:[{
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/1.jpg',
			  title: '送你一朵fua'
			}, {
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/2.jpg',
			  title: '送你一辆车'
			}, {
			  url: 'javascript:',
			  img: 'https://static.vux.li/demo/3.jpg',
			  title: '送你一次旅行'
			}]
		}
	},
  components: {
    XHeader,
    Swiper
  }
}
</script>
<style>
	
</style>