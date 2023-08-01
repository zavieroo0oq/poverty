<template>
	<view class="container">
		<view class="status_bar">
		            <!-- 这里是状态栏 -->
		</view>

			<view class="example-body">
				<uni-row class="demo-uni-row" :width="nvueWidth">
					<uni-col>
						<view class="demo-uni-col dark_deep"></view>
					</uni-col>
				</uni-row>

				<uni-row class="demo-uni-row" :width="nvueWidth">
					<uni-col :span="12">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="12">
						<view class="demo-uni-col light"></view>
					</uni-col>
				</uni-row>

				<uni-row class="demo-uni-row" :width="nvueWidth">
					<uni-col :span="8">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="8">
						<view class="demo-uni-col light"></view>
					</uni-col>
					<uni-col :span="8">
						<view class="demo-uni-col dark"></view>
					</uni-col>
				</uni-row>

				<uni-row class="demo-uni-row" :width="nvueWidth">
					<uni-col :span="6">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="6">
						<view class="demo-uni-col light"></view>
					</uni-col>
					<uni-col :span="6">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="6">
						<view class="demo-uni-col light"></view>
					</uni-col>
				</uni-row>

				<uni-row class="demo-uni-row" :width="nvueWidth">
					<uni-col :span="4">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="4">
						<view class="demo-uni-col light"></view>
					</uni-col>
					<uni-col :span="4">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="4">
						<view class="demo-uni-col light"></view>
					</uni-col>
					<uni-col :span="4">
						<view class="demo-uni-col dark"></view>
					</uni-col>
					<uni-col :span="4">
						<view class="demo-uni-col light"></view>
					</uni-col>
				</uni-row>
			</view>


	</view>
</template>


<script>
	export default {
		data() {
			return {
				gutter: 0,
				nvueWidth: 730
			}	
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.demo-uni-row {
		margin-bottom: 10px;

		// 组件在小程序端display为inline
		// QQ、抖音小程序文档写有 :host，但实测不生效
		// 百度小程序没有 :host
		/* #ifdef MP-TOUTIAO || MP-QQ || MP-BAIDU */
		display: block;
		/* #endif */
	}

	// 支付宝小程序没有 demo-uni-row 层级
	// 微信小程序使用了虚拟化节点，没有 demo-uni-row 层级
	/* #ifdef MP-ALIPAY || MP-WEIXIN */
	::v-deep .uni-row {
		margin-bottom: 10px;
	}

	/* #endif */

	.demo-uni-col {
		height: 36px;
		border-radius: 5px;
	}

	.dark_deep {
		background-color: #99a9bf;
	}

	.dark {
		background-color: #d3dce6;
	}

	.light {
		background-color: #e5e9f2;
	}


	.container{
		height: 100vh;
	}
	.example-body {
		/* #ifndef APP-NVUE */
		display: block;
		/* #endif */
		padding: 5rpx 10rpx 0;
		overflow: hidden;
	}
	
	.status_bar {
	        height: var(--status-bar-height);
	        width: 100%;
	}
</style>


