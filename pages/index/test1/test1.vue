<template>
	<view>
		<button type="primary" @click="set1">setTabBarItem</button>
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
				console.log('setTabBarItem');
				uni.setTabBarItem({
				  index: 0,
				  text: '首页(index)',
				  iconPath: '/static/logo.png',
				  pagePath:'/pages/index/index',
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

</style>
