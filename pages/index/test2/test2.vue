<template>
	<view>
		<button type="primary" @click="set1">setTabBarItem</button>
		<button type="primary" @click="set2">setTabBarStyle</button>
		<button type="primary" @click="set3">hideTabBar</button>
		<button type="primary" @click="set4">showTabBar</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			set1() {
				console.log('setTabBarItem');
				uni.setTabBarItem({
					index: 0,
					text: '首页(index)',
					iconPath: '/static/logo.png',
					pagePath: '/pages/index/index',
					success: () => {
						uni.showToast({
							title: '设置成功'
						})
					},
					fail: (err) => {
						console.log(err);
						uni.showToast({
							icon: 'error',
							title: '设置失败'
						})
					}
				})
			},
			set2() {
				console.log('setTabBarStyle');
				uni.setTabBarStyle({
					color: '#FF0000',
					selectedColor: '#00FF00',
					backgroundColor: '#0000FF',
					borderStyle: 'white',
					success: () => {
						uni.showToast({
							title: '设置成功'
						})
					},
					fail: (err) => {
						console.log(err);
						uni.showToast({
							icon: 'error',
							title: '设置失败'
						})
					}
				})
			},
			set3() {
				console.log('hideTabBar');
				uni.hideTabBar({
					success: () => {
						uni.showToast({
							title: '设置成功'
						})
					},
					fail: (err) => {
						console.log(err);
						uni.showToast({
							icon: 'error',
							title: '设置失败'
						})
					}
				})
			},
			set4() {
				console.log('showTabBar');
				uni.showTabBar({
					success: () => {
						uni.showToast({
							title: '设置成功'
						})
					},
					fail: (err) => {
						console.log(err);
						uni.showToast({
							icon: 'error',
							title: '设置失败'
						})
					}
				})
			}
		}
	}
</script>

<style>
	button {
		margin: 10px;
	}
</style>