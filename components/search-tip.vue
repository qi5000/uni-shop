<template>
	<!-- 搜索框 -->
	<view class="input-box" @tap="toSearch">
		<view class="logo">
			<image src="/static/img/logo.png"></image>
		</view>
		<view class="search-tip">
			<view class="search">
				<image src="/static/img/search.png"></image>
			</view>
			<view class="text">
				{{searchTip}}
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				searchTip: '搜索喜欢的物品',
			};
		},
		methods: {
			toSearch(){
				uni.navigateTo({
					url: '/pages/goods/search'
				})
			}
		}
	}
</script>

<style lang="scss">
.input-box {
	width: 100%;
	height: 60upx;
	background-color: rgba(239,239,239,0.7);
	border-radius: 30upx;
	position: relative;
	display: flex;
	align-items: center;
	.logo{
		height: 52upx;
		width: 180upx;
		vertical-align: middle;
		margin-left: 5upx;
		image{
			width: 100%;
			height: 100%;
		}
	}
	.search-tip{
		position: relative;
		margin-left: 10upx;
		line-height: 28upx;
		padding-left: 10upx;
		font-size: 28upx;
		color: #6d6d6d;
		&::before{
			content: '';
			position: absolute;
			display: inline-block;
			width: 2upx;
			height: 28upx;
			left: 0;
			top: 50%;
			margin-top: -14upx;
			background-color: #dadada;
		}
		.search{
			width: 26upx;
			height: 26upx;
			line-height: 26upx;
			display: inline-block;
			vertical-align: middle;
			margin-right: 10upx;
			image{
				width: 100%;
				height: 100%;
			}
		}
		.text{
			display: inline-block;
			vertical-align: middle;
		}
	}
	.icon {
		display: inline-block;
		font-size: 34upx;
		color: #c0c0c0;
		vertical-align: middle;
		margin: 0 10upx 0 6upx;
	}

}
</style>
