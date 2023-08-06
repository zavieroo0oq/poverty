<template>
	<view class="container">
		<view class="line1">
		<view style="height:7vh;display:flex;align-items: center;">
			<!-- logo与名称 -->
				 <image style="height: 5.5vh;max-height:50px;" mode="heightFix" src="/static/monicaLogo.png" @error="imageError"></image>
				<text style="font-size: 1.4em;font-weight:bold;margin-left: 9px;">汪氏会社</text>
		</view>
		</view>
		
		<view class="line2" style="">
			<text style="font-size: 1.3em;font-weight:600;text-align: left;">流浪狗狗的自主创业</text>
		</view>
		
		<view class="line3">
			
		</view>
		<view class="line4">
			<view style="height: 5vh;"><text>使用以下方式继续</text></view>
			
			<uni-row>
				<uni-col class="btn-box start" :span='12'>
					<view class="giao-btn">
						giao
					</view>
				</uni-col>
				<uni-col class="btn-box end" :span='12'>
					<view class="giao-btn"></view>
				</uni-col>
			</uni-row>
			
			
			<view class="tiaokuan-box" style="height: 15vh;">
				<text class="tiaokuan-line">继续即表示你同意</text>
				<text class="tiaokuan-line" style="margin-top: 6px;"><text id="sytk-btn">使用条款</text>和<text id="yszc-btn">隐私政策</text></text>
			</view>
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
	.line4{
		color:#611fec;
	}
	.giao-btn{
		border: 1px solid rgba(82,0,255);
		border-radius: 4vh;
		height:8vh;
		max-height: 40px;
		width:36vw;
		max-width: 180px;
	}
	.giao-btn:active *{
	  opacity: 0.5;
	}
	.btn-box {
	  display: flex;
	  align-items: center;
	}
	.start {
	  justify-content: flex-start;
	}
	.end {
	  justify-content: flex-end;
	}
	.start .giao-btn {
	  margin-right: auto;
	}
	.end .giao-btn {
	  margin-left: auto;
	}
	.tiaokuan-box {
		display: flex;
		align-items: center;
		flex-direction: column;
		justify-content: center;
	}
	.tiaokuan-line{
		font-size: 0.7rem;
		color: #9da0a3;
		line-height: 1;
	}
	#sytk-btn{
		color:#611fec;
	}
	#yszc-btn{
		color:#611fec;
	}
</style>
