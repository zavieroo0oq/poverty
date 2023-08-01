<template>
	<view class="container">
		<view class="line1">
		<view style="height:7vh;display:flex;align-items: center;">
			<!-- logo与名称 -->
				 <image style="height: 5.5vh;max-height:50px;" mode="heightFix" src="/static/monicaLogo.png" @error="imageError"></image>
				<text style="font-size: 1.4em;font-weight:bold;margin-left: 9px;">Giao</text>
		</view>
		</view>
		
		<view class="line2" style="">
			<text style="font-size: 1.2em;font-weight:600;text-align: left;">你的专属&nbsp;AI&nbsp;助理</text>
		</view>
		
		<view class="line3">
			
		</view>
		<view class="line4">
			<text>使用以下方式继续</text>
			<uni-row>
				<uni-col class="btn-box" :span='11'>
					<view class="giao-btn"></view>
				</uni-col>
				<uni-col class="btn-box" :span='11' :offset="2">
					<view class="giao-btn"></view>
				</uni-col>
			</uni-row>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
			}
		},
		methods: {
		}
	}
</script>

<style>
	.container {
		height: 100vh;
		padding: 0px 20px;
		font-size: 14px;
		line-height: 24px;
	}
	.line1{
		height:20vh;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
	}
	.line2{
		height:8vh;
		display:flex;
		align-items: flex-start;
	}
	.line3{
		height: 45vh;
	}
	.giao-btn{
		border: 1px solid #0043ff;
		border-radius: 3vh;
		height: 40px;
		width: 110px;
	}
	.btn-box{
	}
</style>
