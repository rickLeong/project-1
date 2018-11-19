<template>
	<div class="detail-page">
		<div class="video">
			<video src="http://v3.mukewang.com/shizhan/59f8498ae420e5be578b459b/H.mp4" controls="controls"></video>
		</div>

		<ul class="nav">
			<li v-for="item in arr">{{item}}</li>	
		</ul>

		<div class="title">
			<h1>{{title}}</h1>
			<p>{{des}}</p>
		</div>
		
		<ul class="question">
			<li></li>
		</ul>
		

		<router-link to="/">
			<div class="video-back">＜</div>
		</router-link>
	</div>
</template>

<style scoped>

	.video{
		position: relative;
		height: 190px;
	}

	.video video{
		width: 100%;
		height:100%;
	}

	.video-back{
		background: rgba(0,0,0,0.50);
		border-radius: 2px;
		position: absolute;
		top: 16px;
		left: 36px;
		width: 32px;
		height: 32px;
		font-size: 14px;
		line-height: 32px;
		color: #fff;
		text-align: center;
	}
	.nav{
		background: #FFFFFF;
		box-shadow: 0 2px 4px 0 rgba(0,0,0,0.10);
		height: 44px;
		display: flex;
		justify-content: space-around;
		align-items: center;
	}
	.nav li{
		font-size: 14px;
		color: #71777D;

	}
	.title{
		padding-left: 20px;
		padding-top: 24px;
		box-shadow: 0 8px 4px 0 rgba(0,0,0,0.10);
	}
	.title h1{
		font-size: 16px;
		color: #2B333B;
	}
	.title p{
		font-size: 14px;
		color: #71777D;
		margin-top: 18px;
	}
</style>

<script>
	export default{
		data() {
			return {
				arr:[],
				title:'',
				des:'',
			}
		},
		mounted(){
			this.arr = ['章节','详情','评论','问答','笔记'];
			this.title = 'iOS基础教程之-Camera摄像头';
			this.des =  '从实例出发介绍我们的Camera，可以实现Camera属性检测，照片拍摄，视频录制，图片展示，录制视频';
		}
	}
</script>