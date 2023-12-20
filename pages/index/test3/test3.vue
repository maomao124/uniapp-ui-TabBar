<template>
	<view>
		<button type="primary" @click="set1">setTabBarBadge 1</button>
		<button type="primary" @click="set2">setTabBarBadge 2</button>
		<button type="primary" @click="set3">setTabBarBadge 3</button>
		<button type="primary" @click="set4">removeTabBarBadge 1</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				index1:0,
				index2:0,
				index3:0,
			}
		},
		methods: {
			set1()
			{
				console.log('setTabBarItem');
				uni.setTabBarBadge({
				  index: 0,
				  text: ''+(++this.index1),
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
				uni.setTabBarBadge({
				  index: 1,
				  text: ''+(++this.index2),
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
				uni.setTabBarBadge({
				  index: 2,
				  text: ''+(++this.index3),
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
				uni.removeTabBarBadge({
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
