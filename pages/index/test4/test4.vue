<template>
	<view>
		<button type="primary" @click="set1">showTabBarRedDot 1</button>
		<button type="primary" @click="set2">showTabBarRedDot 2</button>
		<button type="primary" @click="set3">showTabBarRedDot 3</button>
		<button type="primary" @click="set4">hideTabBarRedDot 1</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			}
		},
		methods: {
			set1()
			{
				console.log('showTabBarRedDot');
				uni.showTabBarRedDot({
				  index: 0,
				  success: () => {
				  	uni.showToast({
				  		title:'设置成功'
				  	})
				  },
				  fail: (err) => {
					  console.log(err);
				  	uni.showToast({
				  		icon:'error',
				  		title:'设置失败'
				  	})
				  }
				})
			},
			set2()
			{
				console.log('setTabBarItem');
				uni.showTabBarRedDot({
				  index: 1,
				  success: () => {
				  	uni.showToast({
				  		title:'设置成功'
				  	})
				  },
				  fail: (err) => {
					  console.log(err);
				  	uni.showToast({
				  		icon:'error',
				  		title:'设置失败'
				  	})
				  }
				})
			},
			set3()
			{
				console.log('setTabBarItem');
				uni.showTabBarRedDot({
				  index: 2,
				  success: () => {
				  	uni.showToast({
				  		title:'设置成功'
				  	})
				  },
				  fail: (err) => {
					  console.log(err);
				  	uni.showToast({
				  		icon:'error',
				  		title:'设置失败'
				  	})
				  }
				})
			},
			set4()
			{
				uni.hideTabBarRedDot({
				  index: 0,
				  success: () => {
				  	uni.showToast({
				  		title:'设置成功'
				  	})
				  },
				  fail: (err) => {
					  console.log(err);
				  	uni.showToast({
				  		icon:'error',
				  		title:'设置失败'
				  	})
				  }
				})
			}
		}
	}
</script>

<style>
button{
	margin: 10px;
}
</style>
