<template>
	<view class="uni-container">
		<view class="uni-hello-text">
			<text class="hello-text">uni原生插件示例</text>
		</view>
		<button @click="playVideo1">小屏幕 播放</button>
	</view>
</template>
<script>
	// var TikTok = uni.requireNativePlugin('TiktokUniPlugin');
	var VideoPlayer = uni.requireNativePlugin('VideoPlayerUniPlugin');
	export default {
		data() {
			return {
				list: [{
						id: 'ext-component11',
						name: '小屏 播放器',
						open: false,
						url: '/pages/sample/smallPlayer-component'
					},{
						id: 'ext-module',
						name: '扩展 module',
						open: false,
						url: '/pages/sample/ext-module'
					},
					{
						id: 'ext-component',
						name: '扩展 component',
						open: false,
						url: '/pages/sample/ext-component'
					}, {
						id: 'ext-component 1',
						name: 'splash ad',
						open: false,
						url: '/pages/sample/ext-component1'
					},
					{
						id: 'richAlert',
						name: '插件示例RichAlert',
						open: false,
						url: '/pages/sample/richAlert'
					},
					{
						id: 'UTS_modules',
						name: 'UTS 原生插件',
						open: false,
						url: '/pages/sample/uts_toast'
					}
				],
				navigateFlag: false
			}
		},
		onLoad() {

		},
		methods: {
			playVideo1() {
				uni.navigateTo({
					url: "/pages/sample/smallPlayer-component"
				});
			},
			playVideo() {
				VideoPlayer.playVideo({
					"title": "demo",
					"videoURL": "http://qhxjy.oss-cn-beijing.aliyuncs.com/1751439906853_%E3%80%8A%E4%B8%89%E5%9B%BD%E6%BC%94%E4%B9%89%201994%20%E3%80%8B%E7%AC%AC84%E9%9B%86.mp4",
				});

			},
		}
	}
</script>

<style>
</style>