<template>
	<view class="content">
		<!--直接div可以，組件规范靠近小程序，view是跨平台组件-->
		<view class="globalTestClass">首页</view> 
		<text></text>
		<image></image>
		<button></button>
		<scroll-view scroll-y="true" >
			<view></view>
		</scroll-view>
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
			<swiper-item>
				<view class="swiper-item"></view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item"></view>
			</swiper-item>
		</swiper>
		<!--uni 组件-->
		<uni-tag text="标签发生的范德萨"></uni-tag>
		<uni-countdown :day="1" :hour="1" :minute="12" :second="40"></uni-countdown>
		<uni-table stripe emptyText="暂无更多数据">
			<uni-tr>
				<uni-th align="center"></uni-th>
			</uni-tr>
			<uni-tr>
				<uni-td></uni-td>
			</uni-tr>
		</uni-table>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		// uniapp 页面的生命周期 
		onLoad() {
			// 拿到全局 App.vue 的 globalData 中的数据
			const app = getApp();
			console.log(app.globalData.name)
			
			// 拿到单前页面路由
			 const pages = getCurrentPages()
			 console.log(pages[pages.length-1].route)
		},
		methods: {

		}
	}
</script>

<style>

</style>
