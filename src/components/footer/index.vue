<template>
	<div class="c-footer">
		<ul class="footer-ul">
			<li>
				<img src="../../assets/home.png">
				<span>首页</span>
			</li>
			<li>
				<img src="../../assets/discover.png">
				<span>发现</span>
			</li>
			<li>
				<img src="../../assets/download.png">
				<span>下载</span>
			</li>
			<li>
				<img src="../../assets/me.png">
				<span>我的</span>
			</li>
		</ul>
	</div>
</template>

<style scoped>
	.c-footer{
		position: fixed;
		z-index: 3;
		bottom: 0;
		height: 49px;
		width:375px;
		font-size: 10px;
		color: #2B333B;
		opacity: 0.9;
		background: #FFFFFF;
		box-shadow: inset 0 0.5px 0 0 #D9DDE1;
	}

	.footer-ul{
		display: flex;
		justify-content: space-around;
	}
	.footer-ul li{
		display: flex;
		flex-direction: column;
	}
	.footer-ul img{
		width: 24px;
		height: 24px;
		padding-bottom: 4px;
		padding-top: 6px;
	}

	.footer-ul span{
		display: block;
		padding-bottom: 5px;
	}
</style>

<script>
	export default{}
</script>